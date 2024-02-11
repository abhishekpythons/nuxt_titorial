<script setup>

</script>

<template>
    <div>
        <header class="shadow-sm bg-white">
            <nav class="continer mx-auto p-4 flex justify-between">
                <NuxtLink to="/">Nuxt Dojo</NuxtLink>
                <ul class="flex gap-4">
                    <li>
                        <NuxtLink to="/" class="">Home</NuxtLink>
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


        <div clas="container mx-auto p-4">
            <slot />
        </div>
    </div>
</template>

<style scoped>.router-link-exact-active {
    color: green;
}</style>