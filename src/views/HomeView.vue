<template>
  <div class="splash-container">
    <div class="splash">
      <h1>Splendid Food</h1>
    </div>
  </div>

  <main class="wrapper">

    <h2>Recommended</h2>

    <div class="recommended">
      <ProductContent
        v-for="(product, index) in inventory.slice(0, 3)"
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
  name: 'HomeView',
  props: ['inventory', 'addToCart'],
  components: {
    ProductContent
  }
}
</script>
