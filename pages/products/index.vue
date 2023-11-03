<template>
    <div>
        <h1>Product Home</h1>
        <div v-for="product in product">
            <!-- <NuxtLink :to="`/products/${product.id}`">{{ product.title }}</NuxtLink> -->
            <ProductCard :product="product" />
        </div>
    </div>
</template>

<script setup>

const uri = "https://fakestoreapi.com/products"
const { data: product } = await useFetch(uri)

definePageMeta({
    layout: "products",     
})
</script>

<style scoped>
h1{
    display: flex;
    flex-direction: row;
    justify-content: center;
    font-family: cursive;
}
</style>