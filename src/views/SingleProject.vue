<script>

import axios from 'axios';

export default {


   name: "SingleProject",

   data() {
      return {
         API_URL: 'http://127.0.0.1:8000/',
      }
   },

   /* mounted() {
      axios.get(`${this.API_URL}/api/projects/${this.$route.params.slug}`)
         .then((response) => {
            if (response.data.success) {
               this.project = response.data.project.data;
            } else {
               // redirect alla pagina 404
               this.$router.push({ name: 'not-found' })
            }
         });
   } */

}
</script>
<template>
   <div>

   </div>
</template>


<style lang="scss" scoped></style>