<template>
  
  <div class="header">
    
    <div class="inner">

      <ul class="list">
        
        <li class="item" v-for="item, index in nav_list" :data-hover="item">{{item}}</li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'header',
    data () {
      return {
        nav_list: ['首页', '个人作品', '个人简历', '关于']
      }
    }      
  }
</script>

<style lang="stylus" scoped>
  .header
    width 100%
    height 50px
    line-height 50px 
    background #03a9f4
    .inner
      overflow hidden
      width 1200px
      box-sizing border-box
      margin 0 auto
      .list
        width 100%
        overflow hidden
        .item
          width 150px
          text-align center
          float left
          color #fff
          cursor pointer
          font-size 16px
          position relative
          transition transform .5s
          font-weight 400
          &:hover
            transform translateY(-50px)
          &::before 
            position absolute
            top 50px
            content attr(data-hover)
            transform translate3d(0,0,0)  
</style>