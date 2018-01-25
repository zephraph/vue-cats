<template>
  <img :src="imgUrl" @mousedown="startDrag" @mousemove="drag" @mouseup="stopDrag" :style="positionCSS" class="ViewAccessory" />
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
      isDragging: false,
      top: 0,
      left: 0,
    }
  },
  computed: {
    positionCSS() {
      if (this.isDraggable) {
        return `
          position: absolute;
          top: ${ this.top }px;
          left: ${ this.left }px;
        `
      }

    }
  },
  methods: {
    startDrag(e) {
      console.log("drag started", e);
      const thisAccessory = this.$el
      this.isDraggable = true
      this.isDragging = true;

      // Set current coordinates
      const currentCoords = thisAccessory.getBoundingClientRect()
      this.top = currentCoords.top
      this.left = currentCoords.left

      // thisAccessory.style.top = `${ e.pageX - thisAccessory.offsetWidth / 2 }px`
      // thisAccessory.style.left = `${ e.pageY - thisAccessory.offsetHeight / 2 }px`
    },
    drag(e) {
      // console.log("dragging", e);
      if (this.isDragging) {
        this.top = `${ e.pageY - this.$el.offsetWidth / 2 }px`;
        this.left = `${ e.pageX - this.$el.offsetHeight / 2 }px`;
      }
    },
    stopDrag() {
      console.log("dragging stopped", e);
      this.isDragging = false;
    }
  }
}
</script>

<style>
.ViewAccessory {
  z-index: 1;
}
</style>
