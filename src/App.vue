<template>
  <div id="app">
      <nav-menu></nav-menu>
<!--    <v-header></v-header>-->
      <keep-alive>
        <router-view></router-view>
      </keep-alive>
<!--    <div id="nav">-->
<!--      <router-link to="/">Home</router-link> |-->
<!--      <router-link to="/about">About</router-link>-->
<!--    </div>-->
<!--    <router-view/>-->
  </div>
</template>

<script lang="text/ecmascript-6">
  // import VHeader from 'components/v-header/v-header'
  import NavMenu from 'components/nav-menu/nav-memu'
  export default {
    components: {
      // VHeader
      NavMenu
    }
  }
</script>
<style lang="stylus">

</style>
