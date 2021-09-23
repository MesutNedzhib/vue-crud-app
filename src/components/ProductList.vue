<template>
  <div>
    <p v-if="products.length == 0">Empty Product List</p>
    <table class="table">
      <thead>
        <tr>
          <th>Id</th>
          <th>Product Name</th>
          <th>Category</th>
          <th>Description</th>
          <th>Price</th>
          <th>Stock</th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="product in products" :key="product.id">
          <td>{{ product.id }}</td>
          <td>{{ product.productName }}</td>
          <td>{{ product.categoryId }}</td>
          <td>{{ product.quantityPerUnit }}</td>
          <td>{{ product.unitPrice }}</td>
          <td>{{ product.unitsInStock }}</td>
          <td><button class="btn btn-sm btn-danger" @click="handleDelete(product)">X</button></td>
        </tr>
      </tbody>
    </table>
  </div>
</template>



<script>
export default {
  name: "product-list",
  props: {
    products: Array,
  },
  methods:{
    handleDelete(product){
      this.$emit("delete:product",product)
    },
    handleUpdate(){

    }
  }
};
</script>



<style lang="scss" scoped>
</style>