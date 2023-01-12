<template>
    <div class="metrics_wrapper">
    <div class="metrics">
        <div class="metrics_top">
            <div class="metrics_top_content">
                <h2>Happy customers</h2>
                <p>Since 2017, we have helped thousands of Canadians get their dream vehicles from the comfort of their homes. </p>
            </div>
            <div class="metrics_top_cards">
                <div class="card_item">
                    <h3>7,988+</h3>
                    <p>Sold Cars</p>
                </div>
                <div class="card_item">
                    <h3>16,974+</h3>
                    <p>Vehicles To Choose From</p>
                </div>
            </div>
        </div>
        <div class="metrics_bottom">
            <div class="metrics_bottom_content">
                <p>What are you waiting?</p>
                <p>Get started right now!</p>
                <main-button class="colored">request a car</main-button>
            </div>
            <div class="metrics_bottom_cards">
                <div class="card_item">
                    <h3>123</h3>
                    <p>Experts Across Canada</p>
                </div>
            </div>

        </div>
    </div>
    </div>
</template>
<script>
import MainButton from '@/components/UI/MainButton.vue'
export default {
    components: {
        MainButton
    }
}
</script>

<style lang="scss" scoped>
.metrics_wrapper {
    max-width: 1230px;
    margin: 0 auto;
    height: 336px;
}
.metrics_top {
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.metrics_top_content {
    text-align: start;
    h2 {
        font-weight: 700;
        font-size: 45px;
        line-height: 140.5%;
        color: #41456B;
        margin-bottom: 20px;
    }
    p{
        font-weight: 400;
        font-size: 16px;
        line-height: 180%;
        letter-spacing: 0.02em;
        color: #606276;
        max-width: 549px;
        margin-bottom: 40px;
    }
}
.metrics_top_cards {
    display: flex;
    column-gap: 40px;
}
.card_item {
    width: 280px;
    height: 143px;
    background: #FFFFFF;
    box-shadow: 0px 20px 25px rgba(0, 0, 0, 0.1);
    border-radius: 5px;
}
.metrics_bottom {
    display: flex;
    justify-content: space-between;
}
</style>