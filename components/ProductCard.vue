<template>
  <div>
    <div class="card text-center">
      <img :src="product.image" alt="product thumbnail" class="thumb mx-auto" >
      <p class="font-bold text-gray-500 m-4 truncate">{{ product.title }}</p>
      <NuxtLink :to="`/products/${product.id}`">
        <p class="btn my-4">
          {{ product.title }} 
        </p>
      </NuxtLink> 
    </div>
  </div>
</template>

<script setup>
  const { product } = defineProps(['product'])
</script>

<style scoped>
  .thumb {
    height: 200px;
    object-fit: 'cover'; 
    
  }
</style>