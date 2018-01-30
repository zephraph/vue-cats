<template>
</template>

<script>
export default {
  data() {
    return {
      catParts: [
        [
          'src/assets/heads/cat.png',
          'src/assets/heads/cat1.png',
          'src/assets/heads/cat2.png',
        ],
        [
          'src/assets/torsos/cat.png',
          'src/assets/torsos/cat1.png',
          'src/assets/torsos/cat2.png',
          'src/assets/torsos/cat3.png',
          'src/assets/torsos/cat4.png',
          'src/assets/torsos/cat5.png',
        ],
        [
          'src/assets/legs/cat.png',
          'src/assets/legs/cat1.png',
          'src/assets/legs/cat2.png',
          'src/assets/legs/cat3.png',
          'src/assets/legs/cat4.png',
          'src/assets/legs/cat5.png',
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
