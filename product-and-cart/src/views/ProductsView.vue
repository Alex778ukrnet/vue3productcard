<template>
  <h1>Products</h1>
  <div class="card-container">
    <ProductCard
          v-for="(product, index) in inventory"
          :key="product.id"
          class="card"
          :index="index"
          :product="product"
          :addToCart="addToCart"
        />
  </div>
</template>

<script>
import ProductCard from '@/components/ProductCard.vue'
export default ({
  components: {
    ProductCard
  },
  props: ['inventory', 'addToCart']
})
</script>
