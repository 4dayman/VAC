<template>
    <div class="container">
        <div class="hello_screen">
            <img class="hello_bg" src="@/assets/Bg vector.png" alt="">
            <div class="hello_road">
                <img src="@/assets/Road vector.png" alt="">
            </div>
            <div class="content">
                <div class="content_left">
                    <div class="content_head">
                        The easiest way to buy a car in Canada
                    </div>
                    <main-button class="white max">Request a suv</main-button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import MainButton from '@/components/UI/MainButton.vue'
export default {
    name: 'hello-screen',
    components: {
        MainButton
    }
}
</script>


<style lang="scss" scoped>
    .container {
        width: 100%;
        background: #7481FF;
    }
    .hello_screen {
        position: relative;
        height: 600px;
        transition: all 0.4s ease;
            @media (max-width: 768px) {
                height: 725px;
            }
        .hello_bg {
            position: absolute;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: 0;
        }
    }
    .hello_road {
        position: absolute;
        top: 141px;
        right: 143px;
        max-width: 818px;
        max-height: 394px;
        padding-left: 15px;
        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        @media (max-width: 768px) {
            display: none;
        }
    }
    .content {
        max-width: 1230px;
        padding: 0 15px;
        margin: 0 auto;
    }
    .content_left {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        @media (max-width: 768px) {
            align-items: center;

        }
    }
    .content_head {
        z-index: 1;
        max-width: 534px;
        font-weight: 800;
        font-size: 60px;
        line-height: 108.5%;
        letter-spacing: 0.02em;
        color: #FFFFFF;
        text-align: left;
        margin-top: 120px;
        margin-bottom: 60px;
        @media (max-width: 768px) {
            max-width: 600px;
            text-align: center;
            margin-top: 61px;
        }
    }
    .max {
        width: 200px;
        z-index: 1;
    }
</style>