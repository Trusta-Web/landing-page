<template>
  <footer class="font-Lexend p-4 bg-black sm:p-6 dark:bg-gray-800">
    <div class="mt-10 mb-10 md:mb-0">
      <a href="https://flowbite.com" class="flex items-center">
        <img src="../assets/logo-white.png" class="h-8" alt="FlowBite Logo" />
      </a>
    </div>

    <div class="flex flex-row space-x-5 mt-5 text-white">
      <div class="flex flex-col">
        <div class="space-y-5 mb-5">
          <div class="space-x-5">
            <a href="#" @click="goto('testimony')"> About Us </a>
            <a href="#" @click="goto('porto')"> Our Services </a>
            <a href="#" @click="goto('testimony')"> What our clients say about us </a>
            <a href="#" @click="goto('contact')"> Get in Touch </a>
          </div>
        </div>
      </div>
    </div>

    <div class="sm:flex sm:items-center sm:justify-between">
      <span class="text-sm text-gray-500 sm:text-center dark:text-gray-400"
        >© 2022
        <a href="https://flowbite.com" class="hover:underline">TRUSTA</a>. All
        Rights Reserved.
      </span>
    </div>
  </footer>
</template>

<script>
export default {
   methods: {
    goto(location) {
      var element = document.getElementById(location);
      element.scrollIntoView({ behavior: 'smooth' });
    },
  },
};
</script>

<style></style>
