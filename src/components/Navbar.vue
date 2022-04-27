<template>
  <nav
    class="container flex bg-white mb-2 lg:mb-5 border-gray-200 px-2 sm:px-4 py-2.5 rounded dark:bg-gray-800 font-Lexend"
  >
    <div
      class="container flex flex-wrap justify-between items-center lg:ml-24 mx-auto"
    >
      <a href="#" class="flex items-center">
        <img src="../assets/logo.png" class="h-10" alt="Logo Trusta" />
      </a>
      <div
        class="hidden header3 text-gray-500 w-full md:block md:w-auto"
        id="mobile-menu"
      >
        <ul
          class="flex menu3 flex-col text-xs mt-4 md:flex-row md:space-x-8 md:mt-0 md:text-sm md:font-medium"
        >
          <button @click="goto('testimony')">
            <span
              href="#"
              class="block hover-underline-animation py-2 pr-4 pl-3 border-b border-gray-100 hover:bg-gray-50 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent dark:border-gray-700"
              >About Us</span
            >
          </button>
          <button @click="goto('porto')">
            <span
              href="#"
              class="block hover-underline-animation py-2 pr-4 pl-3 border-b border-gray-100 hover:bg-gray-50 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent dark:border-gray-700"
              >Service</span
            >
          </button><button @click="goto('contact')">
            <span
              href="#"
              class="block hover-underline-animation py-2 pr-4 pl-3 border-b border-gray-100 hover:bg-gray-50 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent dark:border-gray-700"
              >Contact Us</span
            >
          </button>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  methods: {
    goto(location) {
      var element = document.getElementById(location);
      element.scrollIntoView({ behavior: 'smooth' });
    },
  },
};
</script>

<style scoped>
.hover-underline-animation {
  display: inline-block;
  position: relative;
}

.hover-underline-animation:after {
  content: '';
  position: absolute;
  width: 100%;
  transform: scaleX(0);
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: #0087ca;
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
}

.hover-underline-animation:hover:after {
  transform: scaleX(1);
  transform-origin: bottom left;
}
</style>
