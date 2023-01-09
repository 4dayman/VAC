<template>
  <div class="home">
    <HelloScreen/>
    <HowDoesItWork /> 
    <FiveSteps/>
    <Advantages/>
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
import FiveSteps from '@/components/FiveSteps.vue'
import Advantages from '@/components/Advantages.vue'
export default {
  name: 'HomeView',
  components: {
    HelloScreen, HowDoesItWork, FiveSteps, Advantages
  }
}
</script>

<style lang="scss" scoped>
  .home {
    margin-top: 80px;
  }
</style>
