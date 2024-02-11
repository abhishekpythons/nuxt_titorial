<script setup>
    const { id } = useRoute().params
    const uri = `http://fakestoreapi.com/products/${id}`

    // fetch the product
    const { data:product } = await useFetch(uri, { key: id })

    if (!product.value){
        throw createError({statusCode: 404, message: 'Product not found'});
    }
    definePageMeta({
        layout: 'products',
    })
</script>

<template>
    <div>
        <ProductDetails :product="product" />
    </div>
</template>

<style scoped>

</style>