<template>
  <div class="home">
    <HelloScreen/>
    <HowDoesItWork /> 
    <div class="">Home Page</div>
    <nav>
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
    </nav>
  </div>
</template>

<script>
import HelloScreen from '@/components/HelloScreen.vue'
import HowDoesItWork from '@/components/HowDoesItWork.vue'
export default {
  name: 'HomeView',
  components: {
    HelloScreen, HowDoesItWork
  }
}
</script>

<style lang="scss" scoped>
  .home {
    margin-top: 80px;
  }
</style>
