<template>
  <div id="app">
    <Header/>
    <router-view />
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>
    <Footer/>
  </div>
</template>
<script>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'

export default {
    components: {
    Header, Footer
  },
  data() {
        return {
            items: [],
        active: false,
        lock: false,
        }
  },


}
</script>


<style lang="scss">
/* Стили шрифтов */
@import '@/fonts/fonts.css';
// @font-face {
//   font-family: 'Gilroy';
//   src: url('@/fonts/Gilroy-Regular.woff');
//   font-weight: normal;
//   font-style: normal;
// }
/* Обнуление */
@import '@/assets/nullstyle.scss';

#app {
  font-family: 'Gilroy';
  font-style: normal;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 80px;
}
</style>
