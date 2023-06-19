<template>
     <div>  
        <div class="container mx-auto m-4">
            <div class="grid grid-cols-1 gap-4 m-4">
                <a href="#" class="flex flex-col items-center bg-white border border-gray-200 rounded-lg shadow md:flex-row md:max-w-xl hover:bg-gray-100 dark:border-gray-700 dark:bg-gray-800 dark:hover:bg-gray-700">
                    <img class="object-cover w-full rounded-t-lg h-96 md:h-auto md:w-48 md:rounded-none md:rounded-l-lg" :src="products.image" alt="">
                    <div class="flex flex-col justify-between p-4 leading-normal">
                        <h6 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">{{ products.title }}</h6>
                        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">{{ products.description }}</p>
                    </div>
                </a>
            </div>
        </div>
    </div>
</template>
<script setup>
    
    const { id } = useRoute().params
    const url = 'https://fakestoreapi.com/products/'+ id
    const { data : products } = await useFetch(url)
</script>

<style lang="scss" scoped>

</style>