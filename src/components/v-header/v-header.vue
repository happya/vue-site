<template>
  <div class="nav-header">
<!--    <div class="header-wrapper">-->

<!--      <div class="nav">-->
        <router-link tag="div" class="logo" to="/">Ya Yi</router-link>
        <router-link tag="div" class="nav-item" to="/">
          <span>Home</span>
        </router-link>
        <router-link tag="div" class="nav-item" to="/project">
          <span>Project</span>
        </router-link>
        <router-link tag="div" class="nav-item" to="/publication">
          <span>Publication</span>
        </router-link>
<!--        <a class="nav-item" href="http://blog.lionust.tech">Blog</a>-->
<!--      </div>-->
    </div>
<!--  </div>-->
</template>

<script lang="text/ecmascript-6">
  export default {}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  @import "~common/stylus/variable.styl"
  .header
    position: fixed
    left: 0
    top: 0
    width: 100%
    background: $color-background
    height: 5em
    //.header-wrapper
    ///  position: relative
    //  display: flex
     // max-width: 65em
     // width: calc(100% - 6em)
     // height: 100%
     // margin: 0 auto
     // align-items: center

    //.nav
      //display: flex
      //text-align: center
      //margin-left: auto
      //vertical-align: baseline
    .logo
      font-family: 'Pacifico', cursive
      color: $color-font-theme
      font-size: 1.75em
      font-weight: 700
    .nav-item
      flex: 1
      text-transform: uppercase
      font-size: 100%
      line-height: 100%
      padding: 0 0.5em
      font-weight: 400
      color: $color-font-white
</style>
