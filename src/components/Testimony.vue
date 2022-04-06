<template>
  <div class="bg-blue-400 font-Lexend py-5">
    <img
      src="https://media.discordapp.net/attachments/942089520256524362/957623308713599026/unknown.png"
      class="scale-50"
    />
    <p
      class="lg:ml-24 lg:mt-14 mx-auto my-auto text-white lg:text-4xl lg:w-2/5"
    >
      Real Stories from Real Customers
    </p>

    <p class="lg:ml-24 lg:mt-5 mx-auto my-auto text-white lg:text-xl lg:w-2/5">
      Get inspired by these stories.
    </p>
    <swiper
      :slidesPerView="3"
      :spaceBetween="30"
      :freeMode="true"
      :pagination="{
        clickable: true,
      }"
      :modules="modules"
      class="mySwiper mb-20 mt-14"
    >
      <swiper-slide class="mb-5 mx-5 bg-white mt-5 rounded">
        <div class="max-w-sm rounded shadow-lg">
          <div class="px-6 py-4">
            <img
              src="https://media.discordapp.net/attachments/942089520256524362/957511762155020318/unknown.png"
              class="lg:object-scale-down lg:scale-75 lg:w-1/2 w-full"
            />
            <img
              class="lg:object-scale-down lg:scale-50"
              src="https://media.discordapp.net/attachments/942089520256524362/957593155971207218/unknown.png"
            />
            <p class="text-gray-700 text-base ml-2">
              To quickly start my startup landing page design, I was looking for
              a landing page UI Kit. Landify is one of the best landing page UI
              kit I have come across. It’s so flexible, well organised and
              easily editable.
            </p>
            <div class="lg:ml-2 lg:mt-5">
              <pre class="text-lg font-black">Some guy</pre>
            </div>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide class="mb-5 mx-5 bg-white mt-5 rounded">
        <div class="max-w-sm rounded shadow-lg">
          <div class="px-6 py-4">
            <img
              src="https://media.discordapp.net/attachments/942089520256524362/957511762155020318/unknown.png"
              class="lg:object-scale-down lg:scale-75 lg:w-1/2 w-full"
            />
            <img
              class="lg:object-scale-down lg:scale-50"
              src="https://media.discordapp.net/attachments/942089520256524362/957593155971207218/unknown.png"
            />
            <p class="text-gray-700 text-base ml-2">
              To quickly start my startup landing page design, I was looking for
              a landing page UI Kit. Landify is one of the best landing page UI
              kit I have come across. It’s so flexible, well organised and
              easily editable.
            </p>
            <div class="lg:ml-2 lg:mt-5">
              <pre class="text-lg font-black">Some guy</pre>
            </div>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide class="mb-5 mx-5 bg-white mt-5 rounded">
        <div class="max-w-sm rounded shadow-lg">
          <div class="px-6 py-4">
            <img
              src="https://media.discordapp.net/attachments/942089520256524362/957511762155020318/unknown.png"
              class="lg:object-scale-down lg:scale-75 lg:w-1/2 w-full"
            />
            <img
              class="lg:object-scale-down lg:scale-50"
              src="https://media.discordapp.net/attachments/942089520256524362/957593155971207218/unknown.png"
            />
            <p class="text-gray-700 text-base ml-2">
              To quickly start my startup landing page design, I was looking for
              a landing page UI Kit. Landify is one of the best landing page UI
              kit I have come across. It’s so flexible, well organised and
              easily editable.
            </p>
            <div class="lg:ml-2 lg:mt-5">
              <pre class="text-lg font-black">Some guy</pre>
            </div>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide class="mb-5 mx-5 bg-white mt-5 rounded">
        <div class="max-w-sm rounded shadow-lg">
          <div class="px-6 py-4">
            <img
              src="https://media.discordapp.net/attachments/942089520256524362/957511762155020318/unknown.png"
              class="lg:object-scale-down lg:scale-75 lg:w-1/2 w-full"
            />
            <img
              class="lg:object-scale-down lg:scale-50"
              src="https://media.discordapp.net/attachments/942089520256524362/957593155971207218/unknown.png"
            />
            <p class="text-gray-700 text-base ml-2">
              To quickly start my startup landing page design, I was looking for
              a landing page UI Kit. Landify is one of the best landing page UI
              kit I have come across. It’s so flexible, well organised and
              easily editable.
            </p>
            <div class="lg:ml-2 lg:mt-5">
              <pre class="text-lg font-black">Some guy</pre>
            </div>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';

// import required modules
import { Pagination } from 'swiper';

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination],
    };
  },
};
</script>
