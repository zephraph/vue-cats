<template>
  <div class="App">
    <cat-container/>
    <ViewSlider />
    <closet/>
  </div>
</template>

<script>
import CatContainer from './components/CatContainer';
import ViewSlider from './components/ViewSlider'
import Closet from './components/Closet';

export default {
  name: 'app',
  components: {
    CatContainer,
    ViewSlider,
    Closet
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style scoped>
#app {
  margin: 0 auto;
  /* might need to take both of these out later idk */
  display: flex;
  padding: 10px;
}
html, body, .App {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
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
</style>

