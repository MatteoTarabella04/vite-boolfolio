<script>
import ProjectCard from '../components/ProjectCard.vue';

export default {
   name: "AppHome",
   components: { ProjectCard },

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
   <h1 class="text-center">Home page</h1>
   <div class="container">
      <div class="row row-cols-sm-2 row-cols-lg-3">

         <ProjectCard v-for="project in projects" :name="project.name" :description="project.description"
            :link="project.git_hub_link" :project="project" />

      </div>
   </div>
</template>

<style scoped></style>