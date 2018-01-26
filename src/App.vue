<template>
  <div class="App">
    <h1>😸 Vuer</h1>
    <div class="content">
      <CatContainer>
        <ViewSlider v-for="(part, idx) in catParts" :key="idx" />
      </CatContainer>
      <TheCloset/>
    </div>
  </div>
</template>

<script>
import TheCloset from "./components/TheCloset";
import CatContainer from "./components/CatContainer";
import ViewSlider from "./components/ViewSlider";

export default {
  name: "app",
  components: {
    CatContainer,
    TheCloset,
    ViewSlider
  },
  data() {
    return {
      catParts: [
        ["bow", "flower", "glasses", "heart"],
        ["shirt1", "shirt2", "shirt3", "shirt5"],
        ["pants1", "pants2", "pants3", "pants4"]
      ]
    };
  }
};
</script>

<style scoped>
.App {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.content {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin: 0 20px 20px;
  width: calc(100% - 40px);
  height: calc(100% - 20px);
}

.content,
.TheCloset {
  border: 1px dashed black;
}

.TheCloset {
  min-width: 250px;
  background-color: red;
  overflow: auto;
}

.CatContainer {
  width: 100%;
}

h1 {
  text-align: center;
}
</style>
