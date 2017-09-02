<template>
  
  <!-- 个人主页 -->
  <div class="home-page">

    <!-- 头部组件 -->
    <navigation />

  </div>

</template>

<script>

  // 引入头部组件
  import Navigation from '@/components/Header'

  export default {
    name: 'home-page',
    components: {
      Navigation
    },
    data () {
      return {
        
      }
    }
  }
</script>

