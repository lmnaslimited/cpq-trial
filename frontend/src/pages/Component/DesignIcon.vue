<template>
  <div v-for="(icon, index) in icons" :key="index" class="icon-container">
    <div v-html="icon.svgIcon" class="svg-icon"></div>
    <span class="icon-text">{{ icon.label }}</span>
  </div>
</template>

<script>
import { fnGetHomePageData } from './icons.js';

export default {
  data () {
    return {
      icons: fnGetHomePageData('topBarMenus')
    }
  }
}
</script>

<style scoped>
.icon-container {
  display: flex; /* This sets the display type to flex to enable flexbox properties */
  align-items: center; /* This aligns the icon and text vertically in the center */
  margin-right: 10px; /* Add margin to the right side of each icon container */
}

.svg-icon {
  /* Add any specific styles for your icons here */
  width: 24px; /* Example: set a fixed width */
  height: 24px; /* Example: set a fixed height */
  margin-top: 10px; /* Add margin to the top of each icon to adjust its position */
}
</style>
