<template>
  <div class="home">
    <HelloScreen/>
    <HowDoesItWork /> 
    <FiveSteps/>
    <Advantages/>
    <Inventory/>
    <!-- <HeadComp>Some text</HeadComp> -->
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
import Inventory from '@/components/Inventory.vue'
import HeadComp from '@/components/HeadComp.vue'
export default {
  name: 'HomeView',
  components: {
    HelloScreen, 
    HowDoesItWork, 
    FiveSteps, 
    Advantages, 
    Inventory, 
    HeadComp
  }
}
</script>

<style lang="scss" scoped>
  .home {
    margin-top: 80px;
    @media (max-width: 360px) {
      margin-top: 55px;

    }

  }
</style>
