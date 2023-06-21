<script>

import axios from "axios"

export default {
   name: "ProjectCard",
   data() {
      return {
         API_URL: 'http://127.0.0.1:8000/',
         PROJECTS_PATH: 'api/projects',
         projects: [],
      }
   }, methods: {

      getProjects(url) {

         axios.get(url)
            .then(response => {
               this.projects = response.data.projects.data
               console.log(this.projects);
            })
            .catch(error => {
               console.error(error);
            })
      }

   }, mounted() {

      const url = this.API_URL + this.PROJECTS_PATH;
      this.getProjects(url);
   }
}

</script>

<template>
   <div class="col" v-for="project in  projects ">
      <div class="card h-100 p-0">

         <div class="card-body">
            <h3 class="card-title">{{ project.name }}</h3>
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

            <div class="links mb-3">
               <a class="link" target="_blank" :href="project.git_hub_link">{{ project.git_hub_link }}</a>
               <a class="link" v-if="project.page_link" target="_blank" :href="project.page_link">{{ project.page_link
               }}</a>
            </div>

         </div>
         <div class="mb-3 ps-3">
            <router-link :to="{ name: 'single-project', params: { slug: project.slug } }">
               View more...
            </router-link>
         </div>

      </div>
   </div>
</template>

<style scoped>
.card {

   background-color: rgba(7, 11, 49, 0.795);
   border: none;

   color: white;

}

.links {
   .link {
      color: rgb(255, 255, 255);
   }
}
</style>