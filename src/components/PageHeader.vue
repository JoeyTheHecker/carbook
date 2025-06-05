<template>
    <header class="flex justify-center px-6 p-2 bg-amber-500">
        <div class="flex justify-between item-center w-full md:w-5/6 md:relative z-50">
        <PageLogo/>
        <nav class="space-x-6 bg-amber-300">
            <router-link 
                v-for="link in links"
                :key="link.path"
                :to="link.path"
                :class="{'active-link': route.path === link.path}"
                >{{ link.name }}
            </router-link>
        </nav>
    </div>
    </header>
</template>

<script setup>
import PageLogo from './composables/PageLogo.vue';
import { useRoute } from 'vue-router';
//33:23
const route = useRoute();

const links = [
    { name: "Home", path: "/"},
    { name: "About", path: "/about"},
    { name: "Services", path: "/services"},
    { name: "Pricing", path: "/pricing"},
    { name: "Cars", path: "/cars"},
    { name: "Blog", path: "/blog"},
    { name: "Contact", path: "/contact"},
]
</script>