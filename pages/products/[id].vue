<template>   
    <!-- <div class="grid grid-cols-2">
        <div>
            <img :src="product.image" class="w-1/4"alt="Product Image" />
        </div>
        <div>
            <p class="text-md"> {{ product.title }} </p>
            <p class="text-md"> {{ product.price }} </p>
            <p class="text-md"> {{ product.id }} </p>
            <p class="text-md"> {{ product.category }} </p>
            <p class="text-md"> {{ product.description }} </p>
        </div>        
    </div> -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-4 p-4">
    <div class="flex justify-center">
        <img :src="product.image" class="w-full max-w-xs object-contain" alt="Product Image" />
    </div>
    <div class="flex flex-col justify-center">
        <h2 class="text-xl font-semibold mb-2">{{ product.title }}</h2>
        <p class="text-lg text-gray-700 mb-1"><b> Price: </b>{{ product.price }}</p>
        <p class="text-md text-gray-600 mb-1"><b>ID:</b> {{ product.id }}</p>
        <p class="text-md text-gray-600 mb-1"><b>Category:</b> {{ product.category }}</p>
        <p class="text-md text-gray-600 mb-4"><b>Description: </b>{{ product.description }}</p>
        <button class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600 transition duration-200">
            Add to Cart
        </button>
    </div>
</div>

</template>

<script setup>  
   definePageMeta({
        layout: 'products'
    })
    const { id}  = useRoute().params
    const url = "https://fakestoreapi.com/products/"+id;
    const {data: product} = await useFetch(url,{key: id})
</script>

<style scoped>
    img{
        height: 400px;
        width: 350px
    }
</style>