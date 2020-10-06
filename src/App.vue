<template>
  <div id="app">
    <LandingPage/>
  </div>
</template>

<script>
import UIkit from 'uikit'
import Icons from 'uikit/dist/js/uikit-icons'
import LandingPage from './pages/LandingPage.vue'

UIkit.use(Icons)

export default {
  name: 'App',
  components: {
    LandingPage
  }
}
</script>


<style lang="less">
@import "../node_modules/uikit/src/less/uikit.less";
</style>
