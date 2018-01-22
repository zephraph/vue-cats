<template>
  <div class="App">
    <cat-container/>
    <closet/>
  </div>
</template>

<script>
import CatContainer from './components/CatContainer';
import Closet from './components/Closet';

export default {
  name: 'app',
  components: {
    CatContainer,
    Closet
  }
}
</script>

<style>
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
</style>

