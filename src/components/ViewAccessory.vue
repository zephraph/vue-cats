<template>
  <img :src="imgUrl" @dragenter="startDrag" @dragend="dropAccessory" :style="positionCSS" class="ViewAccessory" />
</template>

<script>
export default {
  props: {
    imgUrl: {
      type: String,
      required: true,
    }
  },
  data() {
    return {
      isDraggable: false,
      top: 0,
      left: 0,
    }
  },
  computed: {
    positionCSS() {
      if (this.isDraggable) {
        return `
          position: absolute;
          z-index: 1;
          top: ${ this.top }px;
          left: ${ this.left }px;
        `
      }
    }
  },
  methods: {
    startDrag(e) {
      const thisAccessory = this.$el
      this.isDraggable = true

      // Set current coordinates
      const currentCoords = thisAccessory.getBoundingClientRect()
      this.top = currentCoords.top
      this.left = currentCoords.left

      thisAccessory.style.top = `${ e.pageX - thisAccessory.offsetWidth / 2 }px`
      thisAccessory.style.left = `${ e.pageY - thisAccessory.offsetHeight / 2 }px`

      document.addEventListener('drag', this.changePosition)
    },
    changePosition(e) {
      const thisAccessory = this.$el.style
      if (e.pageX === 0) return

      thisAccessory.top = `${ e.pageY - this.$el.offsetWidth / 2 }px`;
      thisAccessory.left = `${ e.pageX - this.$el.offsetHeight / 2 }px`;
    },
    dropAccessory() {
      document.removeEventListener('drag', this.changePosition)
    }
  }
}
</script>

<style>
.ViewAccessory {
  z-index: 1;
}
</style>
