<template>
    <div>
        <h1>Product About {{ id }}</h1>
        <p>{{ product.title }}</p>
        <p>{{ product.price }}</p>
        <p>{{ product.id }}</p>
    </div>
</template>

<script setup>
const { id } = useRoute().params
const uri = "https://fakestoreapi.com/products/" + id

const { data: product } = await useFetch(uri,{
    key: id
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