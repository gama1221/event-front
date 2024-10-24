<template>
    <div>
        <NuxtLink :to="`/products/${product.id}`" class="block">
            <img 
                :src="product.image" 
                class="w-full h-48 object-contain transition-transform duration-300 transform hover:scale-110" 
                alt="Product Image" 
            />
            <div class="p-4">
                <h3 class="text-lg font-semibold text-gray-800 truncate">{{ product.title }}</h3>
            </div>
        </NuxtLink>
    </div>
</template>

<script setup>
   const { product } = defineProps(["product"])
</script>

<style scoped>

</style>