<script>

import axios from 'axios';

export default {


   name: "SingleProject",

   data() {
      return {
         API_URL: 'http://127.0.0.1:8000/',
         PROJECTS_PATH: 'api/projects',
         project: null,
      }
   },

   mounted() {
      axios.get()
         .then((response) => {
            if (response.data.success) {
               this.project = response.data.project;
               console.log(this.project);
            } else {
               // redirect alla pagina 404
               this.$router.push({ name: 'not-found' })
            }
         })
         .catch(error => {
            console.error(error.message);
         });
   }

}
</script>
<template>
   <div class="container">
      <div class="card m-auto h-100 p-0">
         <div class="card-header">
            <h3 class="card-title">{{ project.name }}</h3>
         </div>
         <div class="card-body">
            <p>
               {{ project.description }}
            </p>
            <p>
               <b v-if="project.technologies">Technologies:</b>
            </p>
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
            <a target="_blank" :href="link">{{ link }}</a>
         </div>
         <div class="card-footer">
         </div>
      </div>
   </div>
</template>


<style lang="scss" scoped></style>