<template>
  <div>
    <!-- Menu Items -->
    <div v-for="(menuItem, index) in fetchedData" :key="index" class="menu-item" @click="handleItemClick(menuItem)">
>
      <div class="menu-text ml-2">{{ menuItem.menu }}</div>
    </div>
  </div>
  <Switch
  size="sm"
  label="Enable Notifications"
  description=""
  :disabled="false"
  v-model="checked"
/>
  
</template>

<script>
import { fnGetHomePageData } from '@/pages/Component/icons.js';

export default {
  data() {
    return {
      fetchedData: null // Initialize the data property
    };
  },
  mounted() {
    // Call the imported function to fetch the data when the component is mounted
    this.fetchDataFromExternalFunction();
  },
  methods: {
    fetchDataFromExternalFunction() {
      // Call the imported function to fetch the data
      this.fetchedData = fnGetHomePageData();
  //     this.fetchedData = [
  //   {menu : 'Adminstrator', icon : 'icon1'},
  //   {menu: 'Dashboard', icon: 'icon2'}


  // ]

    },
    handleItemClick(menuItem) {
      // Handle menu item click here
    }
  }
}
</script>

<style>
.menu-item {
  display: flex;
  align-items: center;
  cursor: pointer;
  padding: 0.5rem 1rem;
}

.menu-icon {
  flex-shrink: 0; /* Prevent icon from shrinking */
  margin-right: 0.5rem; /* Adjust spacing between icon and text */
}

.menu-text {
  flex-grow: 1; /* Allow text to grow to fill remaining space */
}
</style>

