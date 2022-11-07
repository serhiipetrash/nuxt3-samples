<script setup>
//  fetch the products
const { data: products } = await useFetch('https://fakestoreapi.com/products/category/men\'s clothing')

definePageMeta({
  layout: 'products',
})

useHead({
  title: ' Mens clothing',
  meta: [
    { name: 'description', content: 'Mens clothings' },
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
