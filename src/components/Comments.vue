<template>
    <div class="wrapper_comments">
        <div class="comments">
            <h2>What our client say about us!</h2>
            <swiper 
                :slides-per-view="1"
                :space-between="30"
                :loop="false"
                navigation
                grabCursor>
                <swiper-slide class="slide_content">
                        <div class="slide_img">
                            <img src="@/assets/Comments_slide.png" alt="">
                        </div>
                        <div class="slide_text">
                            <h4>Laura Chaisson</h4>
                            <p>In irure et ipsum eiusmod adipisicing id elit cillum proident. Adipisicing ullamco nisi veniam occaecat id excepteur ad non. Sunt occaecat elit ullamco commodo exercitation. Anim mollit irure Lorem proident veniam excepteur non irure Lorem. Lorem esse sint in nisi id esse.</p>
                        </div>
                </swiper-slide>
            </swiper>
        </div>
    </div>
</template>

<script>
import { Navigation } from 'swiper'
import { SwiperCore, Swiper, SwiperSlide } from 'swiper-vue2'
import 'swiper/swiper-bundle.css'

SwiperCore.use([Navigation]);

export default {
    components: {
        Swiper,
        SwiperSlide,
    },
}
</script>

<style lang="scss" scoped>
.wrapper_comments {
    width: 1230px;
    margin: 0 auto;
    padding: 0 15px;
}
.comments{
    // width: 100%;
}
.slide_img{
    max-width: 460px;
    max-height: 322px;
    img{
        width: 100%;height: 100%;
        object-fit: cover;
    }
}


</style>