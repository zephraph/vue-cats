<template>
  <div id="app">
    <ViewSlider />
  </div>
</template>

<script>
import ViewSlider from './components/ViewSlider'

export default {
  name: 'app',
  components: {
    ViewSlider
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style>
#app {
  margin: 0 auto;
}
</style>
