<template>
    <div class="mt-[140px] w-[768px] mx-auto">
        <div class="flex flex-row justify-items-start mb-[24px] w-[1032px] mx-auto ">
            <div class="inline-block">
                <span class="text-[16px] text-[#606266] mr-[13px]">Trang chủ</span>
                <i class="el-icon-arrow-right" />
                <span class="text-[16px] text-[#606266] mr-[13px]">Cá nhân</span>
                <i class="el-icon-arrow-right" />
                <span class="text-[16px] text-[#606266] font-bold">Thông tin cá nhân</span>
            </div>
        </div>
        <div class="mt-[24px] mb-6">
            <img src="@/static/img/themnguoithan.png" class="mx-auto ">
        </div>
        <div class="bg-white flex flex-col justify-items-start mb-[24px] w-[768px] mx-auto p-10">
            <img src="@/static/img/moiquanhe.png" class="w-[101px] h-[38px]">
            <span class="mt-4 text-[16px] text-[#252733]">Xưng - Gọi</span>
            <SelectOption />
        </div>
    </div>
</template>
<script>
    import SelectOption from '@/components/UI/SelectOption.vue';

    export default {
        components: {
            SelectOption,
        },
        layout: 'profile',
    };
</script>
<style scoped>

</style>
