<script>
export default {
   name: "ProjectCard",
   props: {
      name: String,
      link: String,
      description: String,
   }
}

</script>

<template>
   <div class="col">
      <div class="card p-0">
         <div class="card-header">
            <h3 class="card-title">{{ name }}</h3>
         </div>
         <div class="card-body">
            <p>
               {{ description }}
            </p>
            <a target="_blank" :href="link">{{ link }}</a>
         </div>
      </div>
   </div>
</template>