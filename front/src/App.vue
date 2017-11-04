<template>
  <div id="app" class="container">
    <navbar> </navbar>
    <router-view></router-view>

  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
  export default {
  components:{
    'navbar': NavBar
  }
}
</script>

<style lang="scss">

</style>
