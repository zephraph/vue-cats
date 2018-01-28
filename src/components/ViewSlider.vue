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
      if (this.currentIdx) --this.currentIdx;
    },
    scrollRight() {
      if (this.currentIdx < this.images.length - 1) ++this.currentIdx;
    }
  }
};
</script>

<style scoped>
img {
  height: 100%;
}

.ViewSlider {
  display: flex;
  height: calc(100%/3);
  justify-content: space-between;
}
</style>
