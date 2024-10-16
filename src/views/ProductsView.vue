<template>
    <main class="wrapper">
        <h1>Products</h1>

        <div class="card-container">
          <ProductContent
            v-for="(product, index) in inventory.slice(0, 6)"
            :key="product.id"
            :addToCart="addToCart"
            class="card"
            :index="index"
            :product="product"
          />
        </div>
      </main>
</template>

<script>
import ProductContent from '@/components/ProductContent.vue'

export default {
  props: ['inventory', 'addToCart'],
  components: {
    ProductContent
  }
}
</script>
