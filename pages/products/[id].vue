<template>
    <div>
        <h1>Product About {{ id }}</h1>
    </div>
</template>

<script setup>
const { id } = useRoute().params
</script>

<style scoped>
h1{
    display: flex;
    flex-direction: row;
    justify-content: center;
    font-family: cursive;
}
</style>