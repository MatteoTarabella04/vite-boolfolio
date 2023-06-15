<script>
export default {
   name: "ProjectCard",
   props: {
      project: Object,
      name: String,
      link: String,
      description: String,
   }
}

</script>

<template>
   <div class="col">
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