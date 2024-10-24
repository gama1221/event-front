<template>
    <div>
        <header class="shadow-md bg-white">
            <nav class="container mx-auto p-4 flex justify-between">
                <NuxtLink to="/" class="font-bold text-[#16AF90]">ET Event</NuxtLink>
                <ul class="flex gap-4">
                    <li>
                        <NuxtLink to="/">Home</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/about">About</NuxtLink>
                    </li>            
                    <li>            
                        <NuxtLink to="/products" class="btn">Products</NuxtLink>
                    </li>                    
                </ul>                
            </nav>
        </header>
        <div class="container p-4">
            <slot />
        </div>
    </div>
</template>

<script>

   
</script>

<style scoped>
    .router-link-exact-active{
        color: #16AF90        
    }
</style>