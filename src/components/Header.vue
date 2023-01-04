<template>
<div class="container" :class="{lock}">
    <header class="header">
        <div class="header_logo">
            <router-link to="/">
                <img src="@/assets/HeaderLogo.png" alt="">
            </router-link>
        </div>
        <div class="header_menu menu">
            <div>
                <router-link to="/about">
                    <main-button class="white">Inventory</main-button>
                </router-link>
                <router-link to="/">
                    <main-button class="colored">Request a car</main-button>
                </router-link>
            </div>
            <div class="menu_icon" @click="active = !active, bodyLock" :class="{active}">
                <span></span>
            </div>
            <div class="menu_body_shadow" @click="active = !active" :class="{active}"></div>
            <nav class="menu_body" :class="{active}">
                <ul class="menu_list">
                    <li><a href="index.html" class="menu_link">Contact us</a></li>
                    <li><a href="projects.html" class="menu_link">About VAC</a></li>
                    <li><a href="about.html" class="menu_link">Lean Rates</a></li>
                    <li><a href="news.html" class="menu_link">Video</a></li>
                    <li><a href="contacts.html" class="menu_link">Blog</a></li>
                    <li><a href="#popup" class="btn_send_1">Calculate</a></li>
                </ul>
                <div class="menu_social">
                    <a href="#">
                        <img src="@/assets/socialIcons/Instagram.svg" alt="">
                    </a>
                    <a href="#">
                        <img src="@/assets/socialIcons/Facebook.svg" alt="">
                    </a>
                    <a href="#">
                        <img src="@/assets/socialIcons/YouTube.svg" alt="">
                    </a>
                </div>
            </nav>
        </div>
    </header>  
</div>
</template>

<script>
import MainButton from '@/components/UI/MainButton.vue'
export default {
    components: {
        MainButton
    },
    data() {
        return {
            items: [],
        active: false,
        lock: false,
        }
    },
    methods: {
        bodyLock() {
            document.body.classList.toggle('lock');
        }
    }
};
</script>

<style lang="scss" scoped>
body.lock {
    overflow: hidden;
}
.container {
    position: fixed;
    top: 0;
    width: 100%;
    padding: 0 15px;
    margin: 0 auto;
    transition: all 0.5s ease 0.1s;
    @media (max-width: 768px) {
        padding: 0 24px;
    }
}

.header {
    margin: 0 auto;
    position: relative;
    max-width: 1230px;
    height: 80px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    transition: all 1.5 ease 0;
    background: rgba(255, 255, 255, 0.8);
    z-index: 1;
}
.header_fixed {
    width: 100%;
    height: 60px;
    position: fixed;
    top: 0px;
    background: linear-gradient(180deg, #999, #666, #999);
    z-index: 3;
}

.header_logo {
    width: 112px;
    height: 33px;
}
.header_menu{
    display: flex;
    justify-content: flex-end;
    align-items: center;
}
.menu_icon {
    z-index: 5;
    display: block;
    position: relative;
    align-items: center;
    width: 37px;
    height: 30px;
    cursor: pointer;
    margin-left: 63px;
}

.menu_icon span,
.menu_icon::before,
.menu_icon::after {
    right: 0;
    position: absolute;
    height: 4px;
    width: 100%;
    transition: all 0.3s ease 0s;
    background: #41456B;
    border-radius: 7px;
}



.menu_icon::before, .menu_icon::after {
    content: "";
    width: 37px;
}

.menu_icon::before {
    content: "";
    top: 0;
}

.menu_icon::after {
    content: "";
    bottom: 0;
}

.menu_icon span {
    height: 4px;
    top: 50%;
    transform: scale(1) translate(0px, -50%);
}
.menu_icon.active {
    top: 0px;
    right: 0px;
}

.menu_icon.active span {
    transform: scale(0) translate(0px, -50%);
}

.menu_icon.active::before {
    display: block;
    width: 37px;
    top: 50%;
    transform: rotate(-45deg) translate(0px, -50%);
    background-color: #41456B;
}

.menu_icon.active::after {
    width: 37px;
    bottom: 50%;
    transform: rotate(45deg) translate(0px, 50%);
    background-color: #41456B;
}
.menu_body_shadow {
    position: fixed;
    display: none;
    top: 0;
    left:0;
    z-index: 3;
    width: 100%;
    height: 100%;
}
.menu_body_shadow.active {
    display: block;
}
.menu_body {
    position: fixed;
    top: 0;
    right: -100%;
    width: 42%;
    height: 100%;
    background: #fff;
    padding: 130px 0px 105px 60px;
    z-index: 4;
    transition: right 0.3s ease 0s;
    overflow: auto;
    display: flex;
    align-items: flex-start;
    flex-direction: column;
    justify-content: space-between;
    box-shadow: 0px 0px 50px rgba(0, 0, 0, .1);
}
.menu_body.active {
    right: 0;
}
.menu_body.active::before {
    content: "";
    position: fixed;
    top: 0;
    right: 0;
    width: 42%;
    height: 80px;
    background: #fff;
    z-index: 3;
}
.menu_list {
    li{
        text-align: start;
        margin-bottom: 20px;
        font-weight: 700;
        font-size: 25px;
        line-height: 140%;
        letter-spacing: 0.02em;
        a {
            color: #41456B;
        }
    }
}
.menu_social {
    img{
        margin-right: 10px;
        width: 30px;
        height: 30px;
        &:hover {
            opacity: 0.8;
        }
    }
}


/* Old menu */
// .menu__list_body{
//     display: flex;
//     flex-direction: column;
//     justify-content: space-between;
// }
// .menu_list{
//     display: flex;
//     flex-direction: column;
//     gap: 20px;
//     align-items: flex-start;
//     position: absolute;
//     top: 0px;
//     right: 0;
//     padding-top: 130px;
//     padding-left: 60px;
//     min-width: 570px;
//     height: 100vh;
//     background: #fff;
//     z-index: 1;
//     li {
//         font-family: 'Gilroy';
//         font-style: normal;
//         font-weight: 700;
//         font-size: 25px;
//         line-height: 140%;
//         letter-spacing: 0.02em;
//         color: #41456B;
//         cursor: pointer;
//     }
// }
// .modal-backdrop{
//     position: absolute;
//     top: 0;
//     right: 0;
//     left: 0;
//     bottom: 0;
//     height: 100vh;
//     background: rgba(0, 0, 0, 0.1);
// }
// .menu__social__icons{
//     margin-top: 40%;
// }
// .fade{
//     height: 100%;
// }
// .logo{
//     min-width: 112px;
//     max-height: 33px;
//     margin-right: 10px;
// }
// .header__wrapper{
//     position: fixed;
// }
// .header {
//     display: flex;
//     align-items: center;
//     justify-content: space-between;
//     position: fixed;
//     width: 100%;
//     background: rgba(255, 255, 255, 0.9);
// }
// .header__right{
//     display: flex;
//     justify-content: flex-end;
//     align-items: center;
// }
// .btn{
//     font-family: 'Gilroy';
//     font-weight: 700;
//     font-size: 16px;
//     line-height: 14px;
//     text-align: center;
//     letter-spacing: 0.02em;
//     text-transform: uppercase;
//     border: 1px solid #7481FF;
//     border-radius: 2px;
//     margin-right: 10px;
//     padding: 16px 17px;
// }
// .primary{
//     color: #7481FF;
//     background-color: #FFFFFF;
// }
// .accent{
//     color: #FFFFFF;
//     background-color: #7481FF;
// }
// .material-icons{
//     color: #41456B;
//     font-size: 50px;
//     z-index: 2;
//     cursor: pointer;
// }
</style>