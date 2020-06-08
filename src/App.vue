<template>
  <div id="app" class="container mx-auto py-4 lg:py-16">
    <nav class="navigation w-11/12 mx-auto flex justify-between text-center text-white lg:w-1/2">
      <router-link to="/" class="relative w-1/3 px-4 py-2 lg:text-xl" exact>Home</router-link>
      <router-link to="/examples" class="relative w-1/3 px-4 py-2 lg:text-xl">Examples</router-link>
      <router-link to="/contacts" class="relative w-1/3 px-4 py-2 lg:text-xl">Contacts</router-link>
    </nav>
    <main class="main w-11/12 mx-auto mt-8 bg-white">
      <transition>
        <router-view/>
      </transition>
    </main>
    <footer class="text-white text-center mt-8">
      <a href="mailto:teo.reat@gmail.com" class="mr-4 pl-6 lg:ml-8 lg:pl-8 mail relative">teo.reat@gmail.com</a>
    </footer>
  </div>
</template>

<script></script>

<style>
  .navigation > .router-link-active::after {
    bottom: -35px;
    transition: .5s;
  }

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
</style>
