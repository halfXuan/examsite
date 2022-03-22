<template>
  <div class="home">
    <top-header />
  </div>
</template>

<script>
// @ is an alias to /src
import TopHeader from '../components/topHeader.vue'
export default {
  name: 'Home',
  components: {
    TopHeader
  }
}
</script>
<style lang="less" scoped>
.home{
  height: 100vh;
  padding-top: 64px;
}
</style>
