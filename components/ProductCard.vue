<template>
    <div>
        <img :src="`{product.image}`"/>
        <p>{{ product.title }}</p>
        <p>{{ product.rating.rate }}</p>
        <NuxtLink :to="`/products/${product.id}`"><p>View Details</p></NuxtLink>
    </div>
</template>

<script setup>
const { product } = defineProps(['product'])
</script>

<style scoped>

</style>