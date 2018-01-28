<template>
  <div id="app">
    <TheCatContainer />
    <TheCloset />
  </div>
</template>

<script>
import TheCloset from "./components/TheCloset";
import TheCatContainer from "./components/TheCatContainer";

export default {
  name: "app",
  components: {
    TheCatContainer,
    TheCloset,
  }
}
</script>

<style>
/* Reset CSS  */
*,
*:before,
*:after {
  box-sizing: border-box;
}
html, body, .app {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}
</style>

<style scoped>
#app {
  display: flex;
  height: 100%;
}
.TheCloset {
  min-width: 250px;
  overflow: auto;
  width: 25%;
}
.TheCatContainer {
  width: 75%;
}
</style>
