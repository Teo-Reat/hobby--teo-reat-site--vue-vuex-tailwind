<template>
  <div id="app" class="container mx-auto py-4 lg:py-16">
    <nav class="navigation w-11/12 mx-auto flex justify-between text-center text-white lg:w-1/2">
      <router-link to="/" class="relative w-1/4 px-4 py-2 lg:text-xl" exact>Home</router-link>
      <router-link to="/examples" class="relative w-1/4 px-4 py-2 lg:text-xl">Examples</router-link>
      <router-link to="/tools" class="relative w-1/4 px-4 py-2 lg:text-xl">Tools</router-link>
      <router-link to="/contacts" class="relative w-1/4 px-4 py-2 lg:text-xl">Contacts</router-link>
    </nav>
    <main class="main w-11/12 mx-auto bg-white mt-8">
      <router-view/>
    </main>
    <footer class="text-white text-center mt-8">
      <a href="tg://resolve?domain=Teo_Rea" class="mr-4 pl-6 lg:mr-8 lg:pl-8 telegram relative">@Teo_Reat</a>
      <a href="mailto:teo.reat@gmail.com" class="mr-4 pl-6 lg:ml-8 lg:pl-8 mail relative">teo.reat@gmail.com</a>
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
  .telegram::before,
  .mail::before {
    content: url("../src/assets/img/icons/envelope-regular.svg");
    display: block;
    position: absolute;
    width: 20px;
    height: 20px;
    top: 0;
    left: 0;
    filter: invert(1);
  }
  .telegram::before {
    content: url("../src/assets/img/icons/telegram-plane-brands.svg");
    top: -2px;
  }
</style>
