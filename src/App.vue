<template>
  <div id="app">
    <div class="stage">
      <input v-if="!catName" v-model="catName" placeholder="Name your cat" />
      <TheCatContainer />
    </div>
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
  },
  data() {
    return {
      catName: ''
    }
  },
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
  flex-direction: column;
  height: 100%;
}

.stage {
  display: flex;
  flex-direction: column;
  height: 100%;
  justify-content: space-between;
}

.stage,
.TheCloset {
  border: 1px solid black;
}

input {
  font-size: 2rem;
}

.TheCloset {
  min-width: 250px;
  overflow: auto;
}

.TheCatContainer {
  width: 100%;
}

h1 {
  text-align: center;
}
</style>
