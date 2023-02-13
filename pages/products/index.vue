<template>
  <div>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="p in products" :key="p.id">
        <ProductCard :product="p" ></ProductCard>
      </div>
    </div>
  </div>
</template>

<script setup>
  // fetch the products
  const { data: products} = await useFetch('https://fakestoreapi.com/products')

  useHead({
    title: 'Product | Merch',
    meta: [
      { name: 'description', content: 'product page in nuxt'}
    ]
  })
</script>