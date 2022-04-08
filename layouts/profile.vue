<template>
    <div class="bg-[#FEF9F2]">
        <div class="fixed">
            <Header />
        </div>
        <div class=" flex">
            <Sildebar />
            <nuxt />
        </div>
    </div>
</template>
<script>
    import Sildebar from '@/components/shared/Sidebar.vue';
    import Header from '@/components/shared/Header.vue';

    export default {
        components: {
            Sildebar,
            Header,
        },
    };
</script>
<style>
    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
</style>
