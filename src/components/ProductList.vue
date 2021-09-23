<template>
  <div>
    <p v-if="products.length == 0">Empty Product List</p>
  
  </div>
</template>



<script>
export default {
  name: "product-list",
  props: {
    products: Array,
  },
};
</script>



<style lang="scss" scoped>
</style>