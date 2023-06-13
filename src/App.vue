<script>

import axios from 'axios'

export default {
  data() {
    return {
      API_URL: 'http://127.0.0.1:8000/',
      PROJECTS_PATH: 'api/projects',
      projects: [],
    }
  }, method: {
    getProjects(url) {
      axios.get(url)
        .then(response => {
          console.log(response.data);
        })
        .catch(error => {
          console.error(error);
        })

    }
  }, mounted() {
    const url = this.API_URL + this.PROJECTS_PATH
    console.log(url);
  }
}

</script>

<template>
  <h1>Home page</h1>
</template>

<style scoped></style>
