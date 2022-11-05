<script setup>
const { product } = defineProps(['product'])
</script>

<template>
  <div class="card">
    <div class="grid grid-cols-2 gap-10">
      <div class="p-7">
        <img :src="`${product.image}`" class="mx-auto my-7">
      </div>
      <div class="p-7">
        <h2 class="text-4xl my-7">
          {{ product.title }}
        </h2>
        <p class="text-xl my-7">
          Price - ${{ product.price }}
        </p>
        <h3 class="font-bold border-b-2 mb-4 pb-2">
          Product description:
        </h3>
        <p class="mb-7">
          {{ product.description }}
        </p>
        <button class="btn111 flex items-center text-3xl  px-6 py-3 font-bold">
          <span class="c-yellow  w-20 h-20 hover:opacity-60 mr-2" i-carbon-shopping-cart-plus />
          <span>Add to cart</span>
        </button>

        <button class="btn111 flex items-center px-6 py-3 font-bold">
          <span class="i-twemoji-shopping-cart  bg-sky mr-2 text-3xl" />
          <span>Test</span>
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped>
  img {
    max-width: 400px;
  }
</style>
