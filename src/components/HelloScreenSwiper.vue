<template>
  <div>
    <swiper
      class="swiper_wrapper"
      :slides-per-view="1"
      :space-between="30"
      :loop="false"
      navigation
      grabCursor
      @slideChange="onSlideChange"
    >
      <swiper-slide
        class="slide"
        v-for="image in images"
        :key="image.id"
      >
        <img
          :src="image.imgUrl"
        >
        <main-button>Request a {{ image.model }}</main-button>
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
import MainButton from '@/components/UI/MainButton.vue'
export default {
  components: {
    Swiper,
    SwiperSlide,
    MainButton,
  },
  data() {
    return {
      images: [
        { id: 1, model: 'SUV', imgUrl: require("@/assets/main_swiper/SUV.png") },
        { id: 2, model: 'CAR', imgUrl: require("@/assets/main_swiper/CAR.png") },
        { id: 3, model: 'TRUCK', imgUrl: require("@/assets/main_swiper/TRUCK.png") },
        { id: 4, model: 'VAN', imgUrl: require("@/assets/main_swiper/VAN.png") },
      ],
    }
  },
  methods: {
    onSwiper() {},
    onSlideChange() {
      this.$emit('carModel', this.images.model)
    },
  }

};
</script>

<style lang="scss">
.swiper_wrapper {
  max-width: 600px;
  display: flex;
  overflow: hidden;
  transition: all 0.4s ease;
  @media (max-width: 1024px) {
    max-width: 500px;
  }
  @media (max-width: 768px) {
    max-width: 470px;
  }
  @media (max-width: 460px) {
    max-width: 370px;
  }

}

.swiper-slide {
  padding: 0 70px;
  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
}
.swiper-button-prev,
.swiper-button-next {
    color:#7481FF;
    margin-top: 0;
    transform: translateY(-50%);
    width: 53px;
    height: 53px;
    border-radius: 50%;
    background: #fff;
    transition: opacity .4s ease-in;
    opacity: 0.8;
}
.swiper-button-prev:after,
.swiper-button-next:after {
 font-size: 20px;
 font-weight: 700;

}

</style>