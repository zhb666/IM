<template>
  <div id="app">
    <div class="main">
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
import { mapActions } from 'vuex'
export default {
  //  components: {
  //    mycard
  //  },
   created () {
       this.$store.dispatch('initData')
   }
}
</script>

<style lang="stylus" scoped>
#app
  display: flex
  border-radius 50px
  margin: 20px auto
  width: 1024px
  height: 768px
  background-color: #fff
  .sidebar
    width: 280px
    height: 72px
    background: #2b2c2f
  .main
    flex: 1
    height: 768px
    background: #f2f2f2
</style>
