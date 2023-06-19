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
   <div class="col" v-for="project in projects">
      <div class="card h-100 p-0">
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
            <router-link :to="{ name: 'single-project', params: { slug: project.slug } }" class="btn btn-primary">
               View Project
            </router-link>
         </div>
      </div>
   </div>
</template>