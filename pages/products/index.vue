<template>
    <div>
        <h2 class="text-[#16AF90]">Products</h2>
        <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 gap-5">
            <div v-for="p in products" :key="p.id" class="bg-white rounded-lg shadow-md overflow-hidden transition-transform duration-300">
                <ProductCard :product="p" />                
            </div>
        </div>        
    </div>
</template>

<script setup>
    definePageMeta({
        layout: 'products'
    })
    const {data: products} = await useFetch('https://fakestoreapi.com/products')
</script>

<style scoped>
   
</style>