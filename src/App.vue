<template>
  <div id="app">
    <CatContainer/>
    <TheCloset/>
  </div>
</template>

<script>
import TheCloset from './components/TheCloset';
import CatContainer from './components/CatContainer';

export default {
  name: 'app',
  components: {
    CatContainer,
    TheCloset,
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style>
/* CSS reset stuff */
*,
*:before,
*:after {
  box-sizing: border-box;
}
html, body, #app {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}
</style>


<style scoped>
#app {
  margin: 0 auto;
  /* might need to take both of these out later idk */
  display: flex;
  padding: 10px;
}

.CatContainer, .TheCloset {
  border: 1px dashed black;
  height: 100%;
}
.CatContainer {
  width: 85%;
}
.TheCloset {
  width: 15%;
  background-color: red;
}
</style>

