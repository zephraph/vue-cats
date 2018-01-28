<template>
  <img  class="ViewAccessory" :src="imgUrl" :style="[heightStyle, positionCSS]" @dragenter="startDrag" @dragend="dropAccessory" />
</template>

<script>
export default {
  props: {
    imgUrl: {
      type: String,
      required: true,
    },
    height: {
      type: Number,
      required: true
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
    heightStyle() {
      return {
        height: `${this.height}px`
      };
    },
    positionCSS() {
      if (this.isDraggable) {
        // TODO: Decide if z-index belongs here or in CSS
        return {
          position: 'absolute',
          zIndex: 1,
          top: `${ this.top }px`,
          left: `${ this.left }px`
        }
      }
      return {};
    }
  },
  methods: {
    startDrag(e) {
      // Grab this element:
      const thisAccessory = this.$el

      this.isDraggable = true  // TODO: figure out if we can factor this out or not

      // TODO: check if this can be refactored
      // Set accessory's current position in the data:
      const currentCoords = thisAccessory.getBoundingClientRect()
      this.top = currentCoords.top
      this.left = currentCoords.left

      // Create an event listener that changes the current position on the `drag` event:
      document.addEventListener('drag', this.changePosition)
    },
    changePosition(e) {
      // Prevent the image from jumping to top-left corner of page on mouse-up:
      if (e.pageX === 0) return

      // Update accessory's position:
      this.top = e.pageY - this.$el.offsetHeight / 2;
      this.left = e.pageX - this.$el.offsetWidth / 2;
    },
    dropAccessory() {
      // Clean up `drag` event listener:
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
