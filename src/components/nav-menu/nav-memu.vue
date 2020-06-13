<template>
  <div class="nav-menu">
    <router-link tag="div" class="logo" to="/home">
      <span class="nav-link">Ya Yi</span>
    </router-link>

    <div class="menu-items">
      <router-link tag="div" class="item" to="/home">
        <span class="nav-link">Home</span>
      </router-link>

      <router-link tag="div" class="item" to="/project">
        <span class="nav-link">Project</span>
      </router-link>

      <router-link tag="div" class="item" to="/publication">
        <span class="nav-link">publication</span>
      </router-link>
      <a tag="div" class="item" href="http://blog.lionust.tech">
        <span class="nav-link">Blog</span>
      </a>
    </div>

  </div>
</template>

<script lang="text/ecmascript-6">
  export default {}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  @import '~common/stylus/variable.styl'
  .nav-menu
    display: flex
    height: 5em
    line-height: 5em
    width: 100%
    background: $color-background
    .logo
      font-family: 'Pacifico', cursive
      font-weight: 700
      font-size: 1.75em
      padding: 0 2em
      color: $color-font-theme
    .menu-items
      display: flex
      flex: 1
      padding-left: 30%
      .item
        flex: 1
        margin-left: auto
        text-align: center
        .nav-link
          font-size: .65em
          font-weight: 700
          text-transform: uppercase
          color: $color-font-white-ss
        &.router-link-active
          .nav-link
            color: $color-font-theme
            border-bottom: 2px solid $color-font-theme

</style>
