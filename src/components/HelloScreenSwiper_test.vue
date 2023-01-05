<template>
  <div>
    <swiper
      class="swiper_wrapper"
      :slides-per-view="1"
      :space-between="30"
      :loop="false"
      navigation
      @slideChange="onSlideChange"
    >
      <swiper-slide
        class="slide"
        
      >
        <img
          :src="images_data.imgUrl"
        >
        <main-button>Request a {{ images_data.model }}</main-button>
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
    props: {
        images_data: {
            type: Object,
            default() {
                return {}
            }
        }
    },
  components: {
    Swiper,
    SwiperSlide,
    MainButton,
  },
  data() {
    return {}
  },
  methods: {
    onSwiper() {},
    onSlideChange() {
      this.$emit('carModel', this.images_data.model)
    },
  }

};
</script>
<style lang="scss" scoped>
.swiper_wrapper {
  max-width: 490px;
  display: flex;
  overflow: hidden;
  transition: all 0.4s ease;
  @media (max-width: 1024px) {
    max-width: 400px;
  }
  @media (max-width: 768px) {
    max-width: 370px;
  }
  @media (max-width: 460px) {
    max-width: 270px;
  }

}

.swiper-slide {
  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
}
</style>