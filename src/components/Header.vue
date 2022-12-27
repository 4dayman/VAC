<template>
    <nav class="header">
        <img class="logo" src="@/assets/HeaderLogo.png" alt="logo">
        <div class="header__right">
            <button class="btn primary">inventory</button>
            <button class="btn accent">request a car</button>
            <transition name="fade" mode="out-in">
                <i class="material-icons menu" v-if="!show" @click="show = !show" key="menu">menu</i>
                <i class="material-icons close" v-else @click="show = !show" key="close">close</i>
            </transition>
            <transition mame="fade">
                <ul v-if="show">
                    <li v-for="item in items" >{{ item }}</li>
                </ul>
            </transition>
        </div>
    </nav>
</template>

<script>
export default {
    data: {
        items: [
            'Home',
            'about',
            'blog',
            'map',
            'contacts',
        ],
        show: false,
    },
};
</script>

<style lang="scss" scoped>
.drop{
    li{
        color: #000;

    }
}

.logo{
    min-width: 112px;
    max-height: 33px;
    margin-right: 10px;
}
.header {
    display: flex;
    align-items: center;
    justify-content: space-between;
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
.menu{
    color: #41456B;
    font-size: 50px;
}
</style>