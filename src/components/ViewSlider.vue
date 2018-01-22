<template>
  <div class="ViewSlider">
    <div class="side-button" @click="scrollLeft">👈</div>
    <div class="content">
      <img :src="optionsArr[currentIdx]" />
    </div>
    <div class="side-button" @click="scrollRight">👉</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentIdx: 1,
      optionsArr: [
        'https://www.placecage.com/200/200',
        'https://www.placecage.com/300/300',
        'https://www.placecage.com/500/500',
        'https://www.placecage.com/700/700',
        'https://www.placecage.com/900/900',
      ]
    }
  },
  methods: {
    scrollLeft() {
      if (this.currentIdx) --this.currentIdx
    },
    scrollRight() {
      if (this.currentIdx < this.optionsArr.length - 1) ++this.currentIdx
    }
  }
}
</script>

<style scoped>
.side-button {
  flex-basis: 100%;
}
@media screen and (min-width: 800px) {
  .ViewSlider {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    align-items: center;
    text-align: center;
  }
  .side-button {
    flex: 1;
  }
  .content {
    flex: 7;
  }
}
</style>

