<template>
  <div>
    <div class="corner left"></div>
    <div class="corner right"></div>
    
    <div class="max-w-3xl py-12 mx-auto text-center">
      <h1 class="text-4xl font-bold">Welcome to CPQ Page</h1>
      <p class="text-lg mt-4">CPQ (configure, price, quote) is programming that helps sales representatives and self-service customers quickly generate accurate quotes for configurable products and services.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
}
</script>

<style scoped>
.corner {
  position: fixed;
  width: 300px; /* Adjust the width */
  height: 100%; /* Full height of the page */
  background-color: #f0f0f0; /* Light ash color */
  z-index: -1;
}

.left {
  top: 0;
  left: 0;
}

.right {
  top: 0;
  right: 0;
}
</style>
