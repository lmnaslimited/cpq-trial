<!-- Home.vue -->
<template>
  <div class="w-full h-full">
    <Navbar />
    <div class="h-40 w-fit p-4 ">
      <CustomIcon />
    </div>
  </div>
</template>

<script>


import CustomIcon from '@/pages/Component/CustomIcon.vue';
import Navbar from '@/pages/Component/navbar.vue';

export default {
  components: {
    Navbar,
    CustomIcon
  }
}
</script>
