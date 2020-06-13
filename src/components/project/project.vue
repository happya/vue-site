<template>
<div class="projects">
  <h2 class="title">Project</h2>
  <div class="project-list">
    <div v-for="(pro, index) in plist" :key="index" class="list-wrapper">
      <div class="list-item">
        <div :class="pro.websize"><img :src="pro.picUrl" alt=""></div>
        <h3 class="title">{{pro.name}}</h3>
        <div class="demo" v-if="pro.demo"><span class="demo-link">Demo</span></div>
      </div>
    </div>

  </div>
</div>
</template>

<script lang="text/ecmascript-6">
  export default {
    data() {
      return {
        plist: [
          {
            name: 'Smart Data Labeling, Statistics, and Analytic System',
            picUrl: '/images/projects/tupl1.jpg',
            websize: 'laptop'
          },
          {
            name: 'MeowSic: A vue-based web music application',
            picUrl: '/images/projects/meowsic.gif',
            websize: 'mobile',
            demo: 'http://lionust.tech/music'
          }
        ]
      }
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  @import "~common/stylus/variable"
  .projects
    position: relative
    margin: 10px 20px
    .list-wrapper
      margin: 10px 20px
      .list-item
        .laptop
          width: 500px
          height: 280px
          margin: 0 auto
          img
            width: 100%
            height: 100%
        .mobile
          margin: 0 auto
          width: 200px
          img
            width: 100%
        .title
          padding: 10px 0
        .demo
          display: block
          .demo-link
            background-color: $color-deep-green
            text-transform uppercase
            color: $color-font-white-ss
            padding: 6px 24px
            border-radius: 4px
            font-size: 12px

</style>
