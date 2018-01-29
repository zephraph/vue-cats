<template>
  <div class="ViewSlider">
    
    <button @click="scrollLeft">◀</button>

    <img :src="images[currentIdx]" />
    
    <button @click="scrollRight">▶</button>
    
  </div>
</template>

<script>
export default {
  props: {
    images: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      currentIdx: 0,
    };
  },
  methods: {
    scrollLeft() {
      if (this.currentIdx) --this.currentIdx
      else this.currentIdx = this.images.length - 1
    },
    scrollRight() {
      if (this.currentIdx < this.images.length - 1) ++this.currentIdx
      else this.currentIdx = 0
    }
  }
};
</script>

<style scoped>
img {
  height: 100%;
  display: inline-block;
}

.ViewSlider {
  display: flex;
  justify-content: space-between;
  height: calc(100%/3);
}
</style>
