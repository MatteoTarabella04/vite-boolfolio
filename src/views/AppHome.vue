<script>

import ProjectCard from '../components/ProjectCard.vue';

export default {
   name: "AppHome",
   components: { ProjectCard },
}
</script>

<template>
   <main>
      <section class="intro">
         <div class="logo p-3">
            <img src="../assets/img/logo.svg" alt="logo" height="100">
         </div>
      </section>
      <section class="me_menu">
         <div class="container d-flex">
            <div class="col-6 d-flex flex-column justify-content-between h-100 left">
               <div class="top">
                  <h1>
                     Hello, i'm Matteo
                  </h1>
                  <p>
                     Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore totam ratione illo sapiente, dicta
                     quaerat perspiciatis nisi sunt at quidem?
                  </p>
                  <div class="mt-5">
                     <ul class="list-unstyled py-4">
                        <li>
                           <a href="#about">About</a>
                        </li>
                        <li>
                           <a href="#skills">Skills</a>
                        </li>
                        <li>
                           <a href="#projects">Projects</a>
                        </li>
                     </ul>
                  </div>

               </div>
               <div class="footer mb-5">
                  <div class="links text-white">
                     <ul class="list-unstyled d-flex gap-4">
                        <li>
                           <a target="_blank" href="https://github.com/MatteoTarabella04">
                              <svg xmlns="http://www.w3.org/2000/svg" width="25" height="25" fill="currentColor"
                                 class="bi bi-github" viewBox="0 0 16 16">
                                 <path
                                    d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z" />
                              </svg>
                           </a>
                        </li>
                        <li>
                           <a target="_blank" href="https://www.linkedin.com/in/matteo-tarabella/">
                              <svg xmlns="http://www.w3.org/2000/svg" width="25" height="25" fill="currentColor"
                                 class="bi bi-linkedin" viewBox="0 0 16 16">
                                 <path
                                    d="M0 1.146C0 .513.526 0 1.175 0h13.65C15.474 0 16 .513 16 1.146v13.708c0 .633-.526 1.146-1.175 1.146H1.175C.526 16 0 15.487 0 14.854V1.146zm4.943 12.248V6.169H2.542v7.225h2.401zm-1.2-8.212c.837 0 1.358-.554 1.358-1.248-.015-.709-.52-1.248-1.342-1.248-.822 0-1.359.54-1.359 1.248 0 .694.521 1.248 1.327 1.248h.016zm4.908 8.212V9.359c0-.216.016-.432.08-.586.173-.431.568-.878 1.232-.878.869 0 1.216.662 1.216 1.634v3.865h2.401V9.25c0-2.22-1.184-3.252-2.764-3.252-1.274 0-1.845.7-2.165 1.193v.025h-.016a5.54 5.54 0 0 1 .016-.025V6.169h-2.4c.03.678 0 7.225 0 7.225h2.4z" />
                              </svg>
                           </a>
                        </li>
                        <li>
                           <a href="https://instagram.com/matteo_tarabella" target="_blank">
                              <svg xmlns="http://www.w3.org/2000/svg" width="25" height="25" fill="currentColor"
                                 class="bi bi-instagram" viewBox="0 0 16 16">
                                 <path
                                    d="M8 0C5.829 0 5.556.01 4.703.048 3.85.088 3.269.222 2.76.42a3.917 3.917 0 0 0-1.417.923A3.927 3.927 0 0 0 .42 2.76C.222 3.268.087 3.85.048 4.7.01 5.555 0 5.827 0 8.001c0 2.172.01 2.444.048 3.297.04.852.174 1.433.372 1.942.205.526.478.972.923 1.417.444.445.89.719 1.416.923.51.198 1.09.333 1.942.372C5.555 15.99 5.827 16 8 16s2.444-.01 3.298-.048c.851-.04 1.434-.174 1.943-.372a3.916 3.916 0 0 0 1.416-.923c.445-.445.718-.891.923-1.417.197-.509.332-1.09.372-1.942C15.99 10.445 16 10.173 16 8s-.01-2.445-.048-3.299c-.04-.851-.175-1.433-.372-1.941a3.926 3.926 0 0 0-.923-1.417A3.911 3.911 0 0 0 13.24.42c-.51-.198-1.092-.333-1.943-.372C10.443.01 10.172 0 7.998 0h.003zm-.717 1.442h.718c2.136 0 2.389.007 3.232.046.78.035 1.204.166 1.486.275.373.145.64.319.92.599.28.28.453.546.598.92.11.281.24.705.275 1.485.039.843.047 1.096.047 3.231s-.008 2.389-.047 3.232c-.035.78-.166 1.203-.275 1.485a2.47 2.47 0 0 1-.599.919c-.28.28-.546.453-.92.598-.28.11-.704.24-1.485.276-.843.038-1.096.047-3.232.047s-2.39-.009-3.233-.047c-.78-.036-1.203-.166-1.485-.276a2.478 2.478 0 0 1-.92-.598 2.48 2.48 0 0 1-.6-.92c-.109-.281-.24-.705-.275-1.485-.038-.843-.046-1.096-.046-3.233 0-2.136.008-2.388.046-3.231.036-.78.166-1.204.276-1.486.145-.373.319-.64.599-.92.28-.28.546-.453.92-.598.282-.11.705-.24 1.485-.276.738-.034 1.024-.044 2.515-.045v.002zm4.988 1.328a.96.96 0 1 0 0 1.92.96.96 0 0 0 0-1.92zm-4.27 1.122a4.109 4.109 0 1 0 0 8.217 4.109 4.109 0 0 0 0-8.217zm0 1.441a2.667 2.667 0 1 1 0 5.334 2.667 2.667 0 0 1 0-5.334z" />
                              </svg>
                           </a>
                        </li>
                     </ul>
                  </div>
               </div>
            </div>
            <div class="col-6 right">

               <section id="about">
                  <div class="mb-5 text-end">
                     <img src="https://img.freepik.com/free-psd/3d-illustration-person-with-sunglasses_23-2149436188.jpg"
                        alt="avatar" class="rounded-circle" height="200">
                  </div>

                  <p>
                     Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sunt dignissimos fugiat similique?
                     Consequatur repellat id sint provident fugiat, necessitatibus consequuntur harum maxime quos in eos
                     nam vel quasi a non dicta explicabo atque mollitia, dolores alias quaerat earum aperiam aliquid
                     inventore. Accusantium officia minus dolor officiis sequi corporis assumenda laborum.
                  </p>
                  <p>
                     Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sunt dignissimos fugiat similique?
                     Consequatur repellat id sint provident fugiat, necessitatibus consequuntur harum maxime quos in eos
                     nam vel quasi a non dicta explicabo atque mollitia
                  </p>
                  <p>
                     Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                  </p>

               </section>

               <section id="skills">

                  <div class="card mb-3 border-0 skills_card">
                     <div class="card-body text-white">
                        <h4 class="card-title">Skills</h4>
                        <b>Languages:</b>
                        <div class="languages d-flex flex-wrap mt-2 gap-4 justify-content-center">
                           <img src="../assets/img/html5.png" alt="" height="50">
                           <img src="../assets/img/css.png" alt="" height="50">
                           <img src="../assets/img/js.png" alt="" height="50">
                           <img src="../assets/img/sass.png" alt="" height="50">
                           <img src="../assets/img/php.png" alt="" height="50">
                           <img src="../assets/img/sql.png" alt="" height="50">
                        </div>
                        <b>Frameworks:</b>
                        <div class="frameworks d-flex flex-wrap mt-2 gap-4 justify-content-center">
                           <img src="../assets/img/bootstrap.png" alt="" height="50">
                           <img src="../assets/img/vue.png" alt="" height="50">
                           <img src="../assets/img/vite.png" alt="" height="50">
                           <img src="../assets/img/laravel.png" alt="" height="50">
                        </div>
                        <b>Tools:</b>
                        <div class="tools d-flex flex-wrap mt-2 gap-4 justify-content-center">
                           <img src="../assets/img/git.png" alt="" height="50">
                           <img src="../assets/img/github.png" alt="" height="50">
                           <img src="../assets/img/postman-icon.png" alt="" height="50">
                        </div>
                     </div>
                  </div>

               </section>

               <section id="projects">
                  <h2 class="mb-3 text-white">Projects</h2>
                  <ProjectCard />
               </section>

            </div>
         </div>
      </section>

      <!-- <section>
         <div class="container">

            <div class="row row-cols-sm-2 row-cols-lg-3">

               <ProjectCard />

            </div>

         </div>
      </section> -->
   </main>
</template>

<style scoped>
h1 {
   font-size: 4rem;
   color: white;
}

p {
   color: white;
}

.intro {
   position: fixed;
}

.top {
   position: fixed;
   top: 150px;
   width: 30%;

}

.footer {
   position: fixed;
   bottom: 0;
   width: 30%;

}

.right {
   margin-top: 5rem;
}

.languages,
.frameworks,
.tools {
   background-color: #ffffff;
   border-radius: 1rem;
   padding: 1rem;
   cursor: pointer;
}

.skills_card {
   background-color: #0093E9;
   background-image: linear-gradient(135deg, #0093E9 0%, #8ac8cd 50%, #e89568 100%);

}

a {
   color: white;

   &:hover {
      color: #52cdbc;
   }
}

main {
   height: calc(100vh);
   overflow-y: auto;
   /* remove vh */
}

section {
   margin-bottom: 5rem;
}
</style>