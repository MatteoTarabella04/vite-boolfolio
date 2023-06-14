<script>
export default {

   name: 'AppHeader'

}
</script>
<template>
   <header class="shadow d-flex align-items-center">
      <div class="logo px-2">
         logo
      </div>
      <nav class="nav justify-content-center">
         <RouterLink class="nav-link" :to="{ name: 'home' }" aria-current="page">Home</RouterLink>
         <a class="nav-link" href="#">About</a>
         <a class="nav-link" href="#">Contacts</a>
      </nav>
   </header>
</template>


<style lang="scss" scoped></style>