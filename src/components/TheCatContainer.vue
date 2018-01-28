<template>
  <div class="TheCatContainer">
    <input v-model="catName" :placeholder="catName" />
    <ViewSlider v-for="(part, idx) in catParts" :key="idx" :images="part" />
  </div>
</template>

<script>
import ViewSlider from './ViewSlider';

export default {
  components: {
    ViewSlider
  },
  data() {
    return {
      catName: 'Name your cat',
      catParts: [
        [
          'https://www.placecage.com/100/100',
          'src/assets/heads/01.png',
          'src/assets/heads/02.png'
        ],
        [
          'https://www.placecage.com/100/100',
          'src/assets/torsos/01.png',
          'src/assets/torsos/02.png'
        ],
        [
          'https://www.placecage.com/100/100',
          'src/assets/legs/01.png',
          'src/assets/legs/02.png'
        ]
      ]
    };
  }
};
</script>

<style scoped>
.TheCatContainer {
  display: flex;
  flex-direction: column;
}
input {
  width: 100%;
  font-size: 2rem;
  text-align: center;
}
</style>
