<script setup>
//  fetch the products
const { data: products } = await useFetch('https://fakestoreapi.com/products/category/jewelery')

definePageMeta({
  layout: 'products',
})

useHead({
  title: 'jewelery',
  meta: [
    { name: 'description', content: 'jewelery' },
  ],
})
</script>

<template>
  <div>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="p in products" :key="p.id">
        <ProductCard :product="p" />
      </div>
    </div>
  </div>
</template>
