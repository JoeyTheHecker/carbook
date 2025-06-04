<template>
    <PageLogo/>
        <nav>
            <router-link 
                v-for="link in links"
                :key="link.path"
                :to="link.path"
                :class="{'active-link': route.path === link.path}"
                >{{ link.name }}
            </router-link>
        </nav>
</template>

<script setup>
import PageLogo from './composables/PageLogo.vue';
import { useRoute } from 'vue-router';

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