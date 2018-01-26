<template>
  <div class="ViewSlider">
    <button class="side-button" @click="scrollLeft">◀</button>
    <div class="content">
      <img :src="optionsArr[currentIdx]" />
    </div>
    <button class="side-button" @click="scrollRight">▶</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentIdx: 1,
      optionsArr: [
        "https://www.placecage.com/200/200",
        "https://www.placecage.com/300/300",
        "https://www.placecage.com/500/500",
        "https://www.placecage.com/700/700",
        "https://www.placecage.com/900/900"
      ]
    };
  },
  methods: {
    scrollLeft() {
      if (this.currentIdx) --this.currentIdx;
    },
    scrollRight() {
      if (this.currentIdx < this.optionsArr.length - 1) ++this.currentIdx;
    }
  }
};
</script>

<style scoped>
button.side-button{

}

img {
  height: 100%;
}

.ViewSlider {
  display: flex;
  height: calc(100%/3);
  justify-content: space-between;
  border: red;
}
</style>
