<template>
    <router-link to="">
        <h1 class="uppercase text-xl font-bold cursor-pointer">
            <span>Car</span>
            <span>Book</span>
        </h1>
    </router-link>
</template>

<script>
import { onBeforeMount, onMounted, ref } from 'vue';

export default {
    setup() {
        const isScrolled = ref(false)
        const isMobile = ref(window.innerWidth < 760)

        const handleScroll = () => {
            isScrolled.value = window.scrollY > 0
        }

        onMounted(() => {
            window.addEventListener('scroll', handleScroll)
        })

        onBeforeMount(() => {
            window.removeEventListener('scroll', handleScroll)
        })
    }
}
</script>