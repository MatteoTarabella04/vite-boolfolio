<script>

import axios from "axios"

export default {


   name: "SingleProject",

   data() {
      return {
         API_URL: 'http://127.0.0.1:8000/',
         project: null
      }
   },

   mounted() {

      const url = this.API_URL + 'api/projects/' + this.$route.params.slug;
      console.log(url);

      axios
         .get(url)
         .then((response) => {

            console.log(response);

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

}
</script>
<template></template>


<style lang="scss" scoped></style>