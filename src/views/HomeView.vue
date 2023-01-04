<template>
  <div class="home">
    <div class="">Home Page</div>
      <nav>
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'HomeView',
  components: {
  }
}
</script>

<style lang="scss" scoped>
  .home {
    margin-top: 80px;
  }
</style>
