<template>

</template>

<script>

const domain = 'https://raw.githubusercontent.com/zephraph/vue-cats/testStartingPoint/';

export default {
  data() {
    return {
      accessories: [
        {
          imgUrl: `${domain}/src/assets/accessories/mug.png`,
          height: 100,
        },
        {
          imgUrl: `${domain}/src/assets/accessories/flower.png`,
          height: 100,
        },
        {
          imgUrl: `${domain}/src/assets/accessories/bow.png`,
          height: 100,
        },
        {
          imgUrl: `${domain}/src/assets/accessories/glasses.png`,
          height: 100,
        },
        {
          imgUrl: `${domain}/src/assets/accessories/vue.png`,
          height: 100,
        },
        {
          imgUrl: `${domain}/src/assets/accessories/heart.png`,
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

