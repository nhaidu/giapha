<template>
    <div class="w-[1032px] mx-auto flex flex-col pb-10">
        <div class="w-[1032px] flex flex-row justify-items-start mb-[24px]">
            <div class="inline-block">
                <span class="text-[16px] text-[#606266] mr-[13px]">Trang chủ</span>
                <i class="el-icon-arrow-right mr-[13px]" />
                <span class="text-[16px] text-[#606266] mr-[13px]">Gia phả</span>
                <i class="el-icon-arrow-right mr-[13px]" />
                <span class="text-[16px] text-[#606266] font-bold">Tài liệu</span>
            </div>
        </div>
        <div class="flex flex-row justify-between">
            <span class="text-[36px] font-bold">Khuyến học 2021</span>
            <div>
                <el-input
                    v-model="input"
                    placeholder="Nhập tên để tìm kiếm"
                    suffix-icon="el-icon-search"
                />
            </div>
        </div>
        <div class="text-[16px] font-bold mt-10 flex flex-col">
            <div class="w-[1032px] grid grid-cols-4 gap-4">
                <div class="h-[175px] w-[240px] flex flex-col cursor-pointer bg-white">
                    <img src="@/static/img/hsg.png" class="w-full h-[135px]">
                    <div class="w-full h-10 bg-white flex flex-row">
                        <img src="@/static/img/file.svg" class="mr-3 my-auto ml-10">
                        <span class="text-[14px] leading-10">Lê Văn Anh - HSG - lớp 6</span>
                    </div>
                </div>
                <div class="h-[175px] w-[240px] flex flex-col cursor-pointer bg-white">
                    <img src="@/static/img/hsg.png" class="w-full h-[135px]">
                    <div class="w-full h-10 bg-white flex flex-row">
                        <img src="@/static/img/file.svg" class="mr-3 my-auto ml-10">
                        <span class="text-[14px] leading-10">Lê Văn Anh - HSG - lớp 6</span>
                    </div>
                </div>
                <div class="h-[175px] w-[240px] flex flex-col cursor-pointer bg-white">
                    <img src="@/static/img/hsg.png" class="w-full h-[135px]">
                    <div class="w-full h-10 bg-white flex flex-row">
                        <img src="@/static/img/file.svg" class="mr-3 my-auto ml-10">
                        <span class="text-[14px] leading-10">Lê Văn Anh - HSG - lớp 6</span>
                    </div>
                </div>
                <div class="h-[175px] w-[240px] flex flex-col cursor-pointer bg-white">
                    <img src="@/static/img/hsg.png" class="w-full h-[135px]">
                    <div class="w-full h-10 bg-white flex flex-row">
                        <img src="@/static/img/file.svg" class="mr-3 my-auto ml-10">
                        <span class="text-[14px] leading-10">Lê Văn Anh - HSG - lớp 6</span>
                    </div>
                </div>
                <div class="h-[175px] w-[240px] flex flex-col cursor-pointer bg-white">
                    <img src="@/static/img/hsg.png" class="w-full h-[135px]">
                    <div class="w-full h-10 bg-white flex flex-row">
                        <img src="@/static/img/file.svg" class="mr-3 my-auto ml-10">
                        <span class="text-[14px] leading-10">Lê Văn Anh - HSG - lớp 6</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default {

    };
</script>
<style>
    input.el-input__inner {
        height: 48px;
        width: 677px;
    }
</style>
