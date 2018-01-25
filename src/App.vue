<template>
  <div class="App">
    <div class="Content">
    <h1>😸 Vuer</h1>
    <CatContainer>
      <ViewSlider />
      <ViewSlider />
      <ViewSlider />
    </CatContainer>
    </div>
    <TheCloset/>
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
      msg: "Welcome to Your Vue.js App",
      items: [
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
}

.Content,
.TheCloset {
  border: 1px dashed black;
  height: 100%;
}

.Content {
  width: calc(80% - 10px);
  min-width: 500px;
  margin-right: 10px;
}

.TheCloset {
  width: calc(20% - 10px);
  background-color: red;
}

h1 {
  text-align: center;
}
</style>
