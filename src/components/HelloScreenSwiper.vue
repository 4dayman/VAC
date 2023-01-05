<template>
  <div>
    <swiper
      class="swiper_wrapper"
      :slides-per-view="1"
      :space-between="30"
      :loop="false"
      navigation
    >
      <swiper-slide
        class="slide"
        v-for="image in images"
        :key="image.id"
      >
        <img
          :src="image.imgUrl"
        >
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
// import Swiper core and required modules
import { Navigation, Pagination } from 'swiper'

import { SwiperCore, Swiper, SwiperSlide } from 'swiper-vue2'

// Import Swiper styles
import 'swiper/swiper-bundle.css'

SwiperCore.use([Navigation, Pagination]);

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      images: [
        { id: 1, imgUrl: require("@/assets/main_swiper/SUV.png") },
        { id: 2, imgUrl: require("@/assets/main_swiper/CAR.png") },
        { id: 3, imgUrl: require("@/assets/main_swiper/TRUCK.png") },
        { id: 4, imgUrl: require("@/assets/main_swiper/VAN.png") },
      ],
    }
  }

};
</script>
<style lang="scss" scoped>
.swiper_wrapper {
  max-width: 490px;
  display: flex;
  overflow: hidden;
}

.swiper-slide {
  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
}
</style>