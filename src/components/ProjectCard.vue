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
   <div class="col mb-3" v-for="project in  projects ">
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

                  <span class="badge">
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
               <span class="router_link">View more...</span>
            </router-link>
         </div>

      </div>
   </div>
</template>

<style scoped>
.card {

   background-color: #0093E9;
   background-image: linear-gradient(135deg, #0093E9 0%, #8ac8cd 50%, #e89568 100%);

   border: none;

   color: white;
   transition: 1s;

   &:hover {
      transform: scale(1.05);
   }

}

.badge {
   background-color: #52cdbc;
   cursor: pointer;
}

.links {
   .link {
      color: #ffffff;

      &:hover {

         text-decoration: underline;
      }
   }
}

.router_link {
   color: #ffffff;

   &:hover {
      text-decoration: underline;
   }
}
</style>