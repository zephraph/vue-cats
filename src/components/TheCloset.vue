<template>
  <div class="TheCloset">
    <div v-for="(accessory, idx) in accessories" :key="idx" :style="setHeight(accessory)" class="accessory-box">
      <ViewAccessory :imgUrl="accessory.imgUrl" :height="accessory.height"></ViewAccessory>
    </div>
  </div>
</template>

<script>
import ViewAccessory from './ViewAccessory'

export default {
  components: {
    ViewAccessory,
  },
  data() {
    return {
      accessories: [
        {
          imgUrl: 'src/assets/accessories/mug.png',
          height: 150,
        }, {
          imgUrl: 'https://www.placecage.com/100/100',
          height: 100,
        }, {
          imgUrl: 'src/assets/accessories/glasses.png',
          height: 110
        }
      ]
    }
  },
  methods: {
    setHeight(accessory) {
      return `height: ${ accessory.height }px`
    }
  }
}
</script>

<style scoped>
.TheCloset {
  overflow: scroll;
  text-align: center;
  padding: 2rem 0;
}
.accessory-box {
  margin: 2vh;
}
</style>

