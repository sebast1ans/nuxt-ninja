<template>
  <ProductDetails :product="product"/>
</template>

<script setup>
const { id } = useRoute().params
const uri = `https://fakestoreapi.com/products/${id}`
const { data: product } = await useFetch(uri, { key: id })

definePageMeta({
  layout: 'products'
})


</script>

<style lang="scss" scoped>

</style>
