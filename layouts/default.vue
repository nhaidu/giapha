<template>
    <div class="bg-[#FEF9F2] flex flex-col">
        <div class="fixed z-30">
            <Header />
        </div>
        <div class="mt-[104px]">
            <nuxt />
        </div>
    </div>
</template>
<script>
    import Header from '@/components/shared/Header.vue';

    export default {
        components: {
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
