<template>

</template>

<script>

export default {
  data() {
    return {
      accessories: [
        {
          imgUrl: 'src/assets/accessories/mug.png',
          height: 100,
        },
        {
          imgUrl: 'src/assets/accessories/flower.png',
          height: 100,
        },
        {
          imgUrl: 'src/assets/accessories/bow.png',
          height: 100,
        },
        {
          imgUrl: 'src/assets/accessories/glasses.png',
          height: 100,
        },
        {
          imgUrl: 'src/assets/accessories/vue.png',
          height: 100,
        },
        {
          imgUrl: 'src/assets/accessories/heart.png',
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

