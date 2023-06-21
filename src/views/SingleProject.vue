<script>

import axios from "axios"

export default {


   name: "SingleProject",

   data() {
      return {
         API_URL: 'http://127.0.0.1:8000/',
         project: []
      }
   },

   methods: {
      getSingleProject(url) {

         axios
            .get(url)
            .then((response) => {

               console.log(response.data.result);

               if (response.data.success) {
                  this.project = response.data.result;
               } else {
                  // redirect alla pagina 404
                  this.$router.push({ name: 'not-found' })
               }
            })
            .catch(error => {
               console.error(error.message);
            });

      }
   },

   mounted() {

      const singleUrl = this.API_URL + 'api/projects/' + this.$route.params.slug;

      console.log(singleUrl);

      this.getSingleProject(singleUrl);


   }

}
</script>
<template>
   <div class="container py-4">
      <div class="row">
         <div class="col-6">
            <div class="card h-100 border-0 shadow">
               <div class="card-body">

                  <h1>
                     {{ project.name }}
                  </h1>

                  <ul class="d-flex flex-wrap gap-2 list-unstyled" v-if="project.technologies">
                     <li v-for="tech in project.technologies">

                        <span class="badge bg-primary">
                           {{ tech.name }}
                        </span>

                     </li>
                  </ul>

                  <div v-if="project.type" class="type">
                     <p><b>Type: </b>{{ project.type.name }}</p>
                  </div>

               </div>
            </div>
         </div>

         <div class="col-6">
            <div class="card h-100 border-0 shadow">
               <div class="card-body">
                  <p>
                     {{ project.description }}
                  </p>
               </div>
            </div>
         </div>
      </div>
   </div>
</template>


<style lang="scss" scoped></style>