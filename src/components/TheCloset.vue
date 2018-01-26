<template>
  <div class="TheCloset">
    <div v-for="(accessory, idx) in accessories" :key="idx" :style="setHeight(accessory)" class="accessory-box">
      <ViewAccessory :imgUrl="accessory.imgUrl"></ViewAccessory>
    </div>
  </div>
</template>

<style scoped>
</style>

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
          imgUrl: 'https://www.placecage.com/100/100',
          height: 100,
        }, {
          imgUrl: 'https://www.placecage.com/100/100',
          height: 100,
        }, {
          imgUrl: 'https://www.placecage.com/100/100',
          height: 100,
        },
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

<style>
.TheCloset {
  overflow: scroll;
  text-align: center;
}
.accessory-box {
  /* display: inline-block; */
  margin: 5px;
}
</style>

