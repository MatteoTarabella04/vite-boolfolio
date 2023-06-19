<script>

import ProjectCard from '../components/ProjectCard.vue';

export default {
   name: "AppHome",
   components: { ProjectCard },
}
</script>

<template>
   <h1 class="text-center">Home page</h1>
   <div class="container">
      <div class="row row-cols-sm-2 row-cols-lg-3">

         <ProjectCard />

      </div>
   </div>
</template>

<style scoped></style>