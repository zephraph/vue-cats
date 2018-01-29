<template>
  <img  class="ViewAccessory" :src="imgUrl" :style="[heightStyle, positionCSS]" draggable="false" @mousedown="startDrag" />
</template>

<script>
export default {
  props: {
    imgUrl: {
      type: String,
      required: true
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
      topOffset: 0,
      leftOffset: 0
    };
  },
  computed: {
    heightStyle() {
      return {
        height: `${this.height}px`
      };
    },
    positionCSS() {
      if (this.isDraggable) {
        return {
          position: 'absolute',
          top: `${this.top}px`,
          left: `${this.left}px`
        };
      }
      return {};
    }
  },
  methods: {
    startDrag(e) {
      this.isDraggable = true;

      // Set accessory's current position in the data:
      const currentCoords = this.$el.getBoundingClientRect();
      this.top = currentCoords.top;
      this.left = currentCoords.left;

      // Track the mouse's position on the element
      this.topOffset = e.offsetY;
      this.leftOffset = e.offsetX;

      // Create an event listener that changes the current position on the `drag` event:
      document.addEventListener('mousemove', this.changePosition);
      document.addEventListener('mouseup', this.dropAccessory);
    },
    changePosition(e) {
      // Update accessory's position:
      this.top = e.pageY - this.topOffset;
      this.left = e.pageX - this.leftOffset;
    },
    dropAccessory() {
      // Clean up `mousemove` and `mouseup` event listeners:
      document.removeEventListener('mousemove', this.changePosition);
      document.removeEventListener('mouseup', this.dropAccessory);
    }
  }
};
</script>

<style>
.ViewAccessory {
  z-index: 1;
}
</style>
