<template>
  <div id="app">
    <ProductList @delete:product="deleteProduct" :products="products" />
  </div>
</template>



<script>
import ProductList from "./components/ProductList.vue";

export default {
  name: "App",
  components: {
    ProductList,
  },
  data() {
    return {
      products: [
        {
          id: 1,
          categoryId: 1,
          productName: "Phone",
          quantityPerUnit: "Iphone X",
          unitPrice: 1199.99,
          unitsInStock: 2,
        },
        {
          id: 2,
          categoryId: 2,
          productName: "Phone",
          quantityPerUnit: "Xiaomi Note 10",
          unitPrice: 299.99,
          unitsInStock: 5,
        },
        {
          id: 3,
          categoryId: 3,
          productName: "Phone",
          quantityPerUnit: "Iphone XIII",
          unitPrice: 1799.99,
          unitsInStock: 3,
        },
      ],
    };
  },
  methods:{
    deleteProduct(product){
      this.products = this.products.filter(x=>x.id !== product.id)
    }
  }
};
</script>



<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
