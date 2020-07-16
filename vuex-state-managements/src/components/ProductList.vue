<template>
  <div class="d-flex align-items-stretch flex-wrap">
    <ProductCart v-for="product in products" :key="product.id" :product="product"/>
  </div>
</template>

<script>
import ProductCart from './ProductCart';
export default {
  components: {
    ProductCart
  },
  computed: {
    products() {
      return this.$store.state.products
    }
  },
  mounted() {
    this.$store.dispatch('getProducts');
  }
}
</script>

<style>

</style>