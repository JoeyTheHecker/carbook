<template>
    <section class="bg-cover relative h-screen" :style="{ backgroundImage: `url(${bgImage})`}">
        <div class="container">
            <h1 class="text-center">Welcome to My Website</h1>
            <p class="text-center">This is a template for a simple website.</p>
        </div>
    </section>
</template>

<script setup>
    import bgImage from "../../assets/images/bg_1.jpg"
</script>