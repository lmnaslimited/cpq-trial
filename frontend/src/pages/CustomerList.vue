<!-- CustomerList.vue -->

<template>
  <div class="customer-list">
    <h2>Customer List</h2>
    <ul>
      <li v-for="(customer, index) in customers" :key="index">{{ customer.name }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'CustomerList',
  data() {
    return {
      customers: [
        { id: 1, name: 'John Doe' },
        { id: 2, name: 'Jane Smith' },
        { id: 3, name: 'Bob Johnson' }
        // Add more customer data as needed
      ]
    };
  }
}
</script>

<style scoped>
.customer-list {
  /* Add your styles for the customer list */
}
</style>
