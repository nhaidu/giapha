<template>
    <div class=" relative bg-[#FEF9F2] flex flex-col ">
        <div class="flex flex-row justify-items-start mb-[24px] w-[1032px] mx-auto">
            <div class="inline-block">
                <span class="text-[16px] text-[#606266] mr-[13px]">Trang chủ</span>
                <i class="el-icon-arrow-right" />
                <span class="text-[16px] text-[#606266] ">Sự kiện</span>
                <i class="el-icon-arrow-right" />
                <span class="text-[16px] text-[#606266] font-bold">Tất cả sự kiện</span>
            </div>
        </div>
        <div class="flex flex-row justify-center mb-[34px]">
            <div class="mr-[24px]">
                <button class="w-[416px] h-[48px] bg-[#E79000] text-[#fff] text-[18px] font-bold rounded-[4px]">
                    Thêm sự kiện
                </button>
                <div class=" mt-6">
                    <SmallCalendar />
                </div>
            </div>
            <div class="w-[592px] h-[852px] overflow-x-scroll pl-4 bg-white">
                <AllEvent />
            </div>
        </div>
    </div>
</template>
<script>
    import SmallCalendar from '../../../components/sukien/SmallCalendar.vue';
    import AllEvent from '../../../components/sukien/AllEvent.vue';

    export default {
        components: {
            SmallCalendar,
            AllEvent,
        },
    };
</script>
<style scoped>

</style>
