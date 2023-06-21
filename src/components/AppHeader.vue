<script>
export default {

   name: 'AppHeader'

}
</script>
<template>
   <header class="shadow d-flex align-items-center">
      <div class="logo p-2">
         <img src="../assets/img/Logo_Portfolio.png" alt="logo" height="70">
      </div>
      <nav class="nav justify-content-center">
         <RouterLink class="nav-link" :to="{ name: 'home' }">Home</RouterLink>
         <a class="nav-link" href="#">About</a>
         <a class="nav-link" href="#">Contacts</a>
      </nav>
   </header>
</template>


<style lang="scss" scoped></style>