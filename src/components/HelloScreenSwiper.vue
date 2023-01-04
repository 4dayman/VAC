<template>
  <swiper class="swiper" grabCursor navigation>
    <swiper-slide
        :modules="modules"
        v-for="image in images"
        :key="image.id"
    >
        <img :src="image.imgUrl" />
    </swiper-slide>
  </swiper>
</template>
<script>
  // import Swiper core and required modules
  import { Navigation } from 'swiper';

  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/scss';
  import 'swiper/scss/navigation';

  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    data() {
        return {
            images: [
                {id: 1, imgUrl: require("@/assets/main_swiper/SUV.png")},
                {id: 2, imgUrl: require("@/assets/main_swiper/CAR.png")},
                {id: 3, imgUrl: require("@/assets/main_swiper/TRUCK.png")},
                {id: 4, imgUrl: require("@/assets/main_swiper/VAN.png")},
            ],
            modules: [Navigation],
        }
    }
    
  };
</script>
<style lang="scss" scoped>
.swiper {
    max-width: 490px;
    display: flex;
}
    .swiper-slide {
        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
</style>