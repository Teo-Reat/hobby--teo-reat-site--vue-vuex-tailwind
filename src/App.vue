<template>
  <div id="app" class="container mx-auto py-4 lg:py-16">
    <nav class="navigation w-11/12 mx-auto flex justify-between text-center text-white lg:w-1/3">
      <router-link to="/" class="relative w-24 px-4 py-2 lg:text-xl" exact>Home</router-link>
      <router-link to="/examples" class="relative w-24 px-4 py-2 lg:text-xl">Examples</router-link>
      <router-link to="/contacts" class="relative w-24 px-4 py-2 lg:text-xl">Contacts</router-link>
    </nav>
    <main class="main w-11/12 mx-auto bg-white mt-8">
      <router-view/>
    </main>
    <footer class="text-white text-center mt-8">
      @Teo_Reat
    </footer>
  </div>
</template>

<style>
 .router-link-active::after {
   content: '';
   box-sizing: content-box;
   display: block;
   position: absolute;
   width: 0;
   height: 0;
   background: transparent;
   border-left: 25px solid transparent;
   border-right: 25px solid transparent;
   border-bottom: 25px solid white;
   bottom: -35px;
   left: 26px;
   z-index: -1;
 }
</style>
