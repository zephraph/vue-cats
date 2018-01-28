<template>
  <div class="CatContainer">
    <!-- <slot /> -->
    <ViewSlider v-for="(part, idx) in catParts" :key="idx" :images="part" />
  </div>
</template>

<script>
import ViewSlider from './ViewSlider'

export default {
  components: {
    ViewSlider
  },
  data() {
    return {
      catParts: [
        [
          'https://www.placecage.com/100/100',
          'src/assets/heads/01.png',
          'src/assets/heads/02.png',
        ], [
          'https://www.placecage.com/100/100',
          'src/assets/torsos/01.png',
          'src/assets/torsos/02.png',
        ], [
          'https://www.placecage.com/100/100',
          'src/assets/legs/01.png',
          'src/assets/legs/02.png',
        ],
      ]
    }
  }
}
</script>
