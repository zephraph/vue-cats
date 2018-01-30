<template>
</template>

<script>

const domain = 'https://raw.githubusercontent.com/zephraph/vue-cats/testStartingPoint/';

export default {
  data() {
    return {
      catParts: [
        [
          `${domain}/src/assets/heads/cat.png`,
          `${domain}/src/assets/heads/cat1.png`,
          `${domain}/src/assets/heads/cat2.png`,
        ],
        [
          `${domain}/src/assets/torsos/cat.png`,
          `${domain}/src/assets/torsos/cat1.png`,
          `${domain}/src/assets/torsos/cat2.png`,
          `${domain}/src/assets/torsos/cat3.png`,
          `${domain}/src/assets/torsos/cat4.png`,
          `${domain}/src/assets/torsos/cat5.png`,
        ],
        [
          `${domain}/src/assets/legs/cat.png`,
          `${domain}/src/assets/legs/cat1.png`,
          `${domain}/src/assets/legs/cat2.png`,
          `${domain}/src/assets/legs/cat3.png`,
          `${domain}/src/assets/legs/cat4.png`,
          `${domain}/src/assets/legs/cat5.png`,
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
