<template>
  <div class="bg-blue-500 font-Lexend py-5" >
    <img
      src="https://media.discordapp.net/attachments/942089520256524362/957623308713599026/unknown.png"
      class="scale-50 lg:z-0 lg:scale-50 lg:absolute "
      id="testimony"
    />
    <div class="lg:z-10 lg:relative">
    <p
      class="ml-14 lg:ml-24 lg:mt-14 mx-auto my-auto lg:mt-36 text-white lg:text-5xl lg:w-2/5"
    >
      Real Stories from Real Customers
    </p>
    <p class="ml-14 lg:ml-24 lg:mt-5 mx-auto my-auto text-white lg:text-xl lg:w-2/5">
      Get inspired by these stories.
    </p>
    </div>
    <swiper
      :slidesPerView="3"
      :spaceBetween="30"
      :freeMode="true"
      :pagination="{
        clickable: true,
      }"
      :modules="modules"
      class="invisible lg:visible lg:mySwiper lg:mb-20 lg:mt-14"
    >
      <swiper-slide class="mx-5 bg-white mt-5 rounded" 
      v-for="t in testimony" :key="t.id">
        <div class="rounded">
          <div class="px-6 py-4">
            <img
              :src="t.logo"
            />
            <img
              class="lg:object-scale-down lg:scale-50"
              src="https://media.discordapp.net/attachments/942089520256524362/957593155971207218/unknown.png"
            />
            <p class="text-gray-700 text-base ml-2">
             {{t.testimony}}
            </p>
            <div class="lg:ml-2 lg:mt-5">
              <pre class="text-lg font-black">- {{t.name}}</pre>
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
import axios from 'axios'
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
  data(){
    return {
      testimony: []
    }
  },


  mounted(){
    axios
    .get('https://trusta-be.herokuapp.com/customers')
    .then(res => {
      this.testimony = res.data
    })
    .catch(err => {
      console.log(err)
    })
  }
};
</script>
