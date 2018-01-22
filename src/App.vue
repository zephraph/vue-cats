<template>
<<<<<<< HEAD
  <div id="app">
    <ViewSlider />
=======
  <div class="App">
    <cat-container/>
    <closet/>
>>>>>>> 5d0e1cb7200acb657cc072424cc780852ce0ae20
  </div>
</template>

<script>
<<<<<<< HEAD
import ViewSlider from './components/ViewSlider'
=======
import CatContainer from './components/CatContainer';
import Closet from './components/Closet';
>>>>>>> 5d0e1cb7200acb657cc072424cc780852ce0ae20

export default {
  name: 'app',
  components: {
<<<<<<< HEAD
    ViewSlider
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
=======
    CatContainer,
    Closet
>>>>>>> 5d0e1cb7200acb657cc072424cc780852ce0ae20
  }
}
</script>

<style>
<<<<<<< HEAD
#app {
  margin: 0 auto;
}
=======
  html, body, .App {
    width: 100%;
    height: 100%;
    margin: 0;
    padding: 0;
  }
</style>

<style scoped>
  .App {
    display: flex;
    padding: 10px;
  }
  .CatContainer, .Closet {
    border: 1px dashed black;
  }
  .CatContainer {
    width: calc(75% - 20px);
    margin-right: 10px;
  }
  .Closet {
    width: calc(25% - 10px);
  }
>>>>>>> 5d0e1cb7200acb657cc072424cc780852ce0ae20
</style>

