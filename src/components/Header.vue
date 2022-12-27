<template>
<div class="header__wrapper">
    <nav class="header">
        <img class="logo" src="@/assets/HeaderLogo.png" alt="logo">
        <div class="header__right">
            <button class="btn primary">inventory</button>
            <button class="btn accent">request a car</button>
            <transition name="fade" mode="out-in">
                <i class="material-icons menu" v-if="!show" @click="show = !show" :key="menu">menu</i>
                <i class="material-icons clear" v-else @click="show = !show" :key="clear">close</i>
            </transition>
            <transition mame="fade">
                <ul class="menu_list" v-if="show">
                    <li class="list__item" v-for="item in items" :key="item">{{ item }}</li>
                </ul>
            </transition>
        </div>
    </nav>
</div>

</template>

<script>
export default {
    name: 'header',
    data() {
        return {
            items: [
                'Contact us',
                'About VAC',
                'Lean Rates',
                'Video',
                'Blog',
                'Calculate',
            ],
        show: false,
        }
    },
};
</script>

<style lang="scss" scoped>
// .drop{
//     li{
//         color: #000;

//     }
// }
.list__item{
    font-family: 'Gilroy';
    font-style: normal;
    font-weight: 700;
    font-size: 25px;
    line-height: 140%;
    letter-spacing: 0.02em;
    color: #41456B;
    cursor: pointer;
}
.menu_list{
    display: flex;
    flex-direction: column;
    gap: 20px;
    align-items: flex-start;
    position: absolute;
    top: 0px;
    right: 0;
    padding-top: 130px;
    padding-left: 60px;
    min-width: 570px;
    min-height: 100vh;
    background: #000;
}
.logo{
    min-width: 112px;
    max-height: 33px;
    margin-right: 10px;
}
.header__wrapper{
    position: fixed;
}
.header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: fixed;
    width: 100%;
    background: rgba(255, 255, 255, 0.9);
}
.header__right{
    display: flex;
    justify-content: flex-end;
    align-items: center;
}
.btn{
    font-family: 'Gilroy';
    font-weight: 700;
    font-size: 16px;
    line-height: 14px;
    text-align: center;
    letter-spacing: 0.02em;
    text-transform: uppercase;
    border: 1px solid #7481FF;
    border-radius: 2px;
    margin-right: 10px;
    padding: 16px 17px;
}
.primary{
    color: #7481FF;
    background-color: #FFFFFF;
}
.accent{
    color: #FFFFFF;
    background-color: #7481FF;
}
.material-icons{
    color: #41456B;
    font-size: 50px;
    z-index: 1;
    cursor: pointer;
}
</style>