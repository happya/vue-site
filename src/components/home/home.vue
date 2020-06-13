<template>
 <div class="home">
   <div class="banner"></div>
   <about class="inner-about"></about>
   <div class="links">
     <a  href="cv.pdf"><span class="link-item">Resume</span></a>
     <a  href="https://www.linkedin.com/in/ya-yi-9ab06662/"><span class="link-item">Linkedin</span></a>
     <a  href="https://scholar.google.com/citations?user=Gi3lTyQAAAAJ&hl"><span class="link-item">google scholar</span></a>
   </div>
   <div class="education">
     <h2>Education</h2>
     <div class="education-list" v-for="(uni, index) in edu"
          :key="index">
       <div class="list-item">
         <div class="logo"><img :src="uni.img" alt=""></div>
         <div class="education-right">
           <div class="title">{{uni.name}}</div>
           <div class="time">{{uni.start}}-{{uni.end}}</div>
           <div class="degree">{{uni.degree}}</div>
         </div>
       </div>
     </div>
   </div>
 </div>
</template>

<script lang="text/ecmascript-6">
  import About from 'components/about/about'
  export default {
    data() {
      return {
        edu: [
          {
            img: 'uw.png',
            name: 'University of Washington',
            start: 2019,
            end: 2021,
            degree: 'Master in Electrical & Computer Engineering'
          },
          {
            img: 'hkust.png',
            name: 'Hong Kong University of Science & Technology',
            start: 2012,
            end: 2016,
            degree: 'Ph.D. in Physics'
          }, {
            img: 'whu.png',
            name: 'Wuhan University',
            start: 2008,
            end: 2012,
            degree: 'B.S. in Electronics'
          }
        ]
      }
    },
    components: {
      About
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  @import "~common/stylus/mixin.styl"
  @import "~common/stylus/variable.styl"
  .home
    position: relative
    .banner
      position: relative
      display: block
      width: 100%
      bg-image('banner')
      padding-bottom: 200px
      background-repeat: no-repeat
      background-size: cover
      text-align: left
    .inner-about
      position: relative
      padding: 20px 0 0 20px
      max-width: 65em
      width: calc(100% - 6em)
      margin-right: 20%
    .links
      position: relative
      padding: 20px 20px
      display: flex
      margin-right: 20%
      a
        flex: 1
        text-align: center
        text-transform uppercase
        .link-item
          font-size: 12px
          color: $color-font-theme
          font-weight: 500
          padding: 12px 32px
          border: 2px solid $color-font-theme
    .education
      position: relative
      margin: 20px 20px
      .education-list
        display: flex
        .list-item
          display: flex
          heigth: 100px
          margin-left: 20px
          padding: 10px 0
          .logo
            position: relative
            width: 100px
            height: 100px
            img
              width: 100%
              height: 100%
          .education-right
            display: flex
            line-height: 20px
            padding: 0 16px
            text-align: left
            justify-content center
            flex-direction column
            .title
              font-size: 14px
              text-transform uppercase
              color: $color-font-theme
              font-weight: 700
            .time
              font-size: 12px
              color: $color-deep-blue
            .degree
              font-size: 12px
              color: $color-deep-green
              font-weight: 300
</style>
