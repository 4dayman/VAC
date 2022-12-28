<template>
  <div id="app">
    <router-view/>
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>
  </div>
</template>

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
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
