<template>
    <PageHeader />
    <main>
        <router-view></router-view>
    </main>
    <PageFooter />
</template>

<script>
import PageHeader from './PageHeader.vue';
import PageFooter from './PageFooter.vue';

export default {
    components: {
        PageHeader,
        PageFooter,
    }
}

</script>