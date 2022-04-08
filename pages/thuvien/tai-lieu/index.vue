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
            <span class="text-[36px] font-bold">Tài liệu</span>
            <div class="w-[768px]">
                <el-input
                    v-model="input"
                    placeholder="Nhập tên để tìm kiếm"
                    suffix-icon="el-icon-search"
                />
            </div>
        </div>
        <div class="text-[16px] font-bold mt-10 flex flex-col">
            <span class="mb-6">Thư mục</span>
            <div class=" mb-6 w-[1032px] grid grid-cols-4 gap-4">
                <div class="w-[240px] h-[58px] bg-white rounded-[8px] flex flex-row justify-between cursor-pointer">
                    <div class="flex flex-row ml-5 ">
                        <img src="@/static/img/folder.svg" class="my-auto">
                        <div class=" leading-[58px] ml-4 font-normal truncate ">
                            Thành tích
                        </div>
                    </div>
                    <div class="flex flex-col my-auto mr-3">
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full mb-[3px]" />
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full mb-[3px]" />
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full" />
                    </div>
                </div>
                <div class="w-[240px] h-[58px] bg-white rounded-[8px] flex flex-row justify-between cursor-pointer">
                    <div class="flex flex-row ml-5 ">
                        <img src="@/static/img/folder.svg" class="my-auto">
                        <div class=" leading-[58px] ml-4 font-normal truncate ">
                            Thành tích
                        </div>
                    </div>
                    <div class="flex flex-col my-auto mr-3">
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full mb-[3px]" />
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full mb-[3px]" />
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full" />
                    </div>
                </div>
                <div class="w-[240px] h-[58px] bg-white rounded-[8px] flex flex-row justify-between cursor-pointer">
                    <div class="flex flex-row ml-5 ">
                        <img src="@/static/img/folder.svg" class="my-auto">
                        <div class=" leading-[58px] ml-4 font-normal truncate ">
                            Thành tích
                        </div>
                    </div>
                    <div class="flex flex-col my-auto mr-3">
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full mb-[3px]" />
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full mb-[3px]" />
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full" />
                    </div>
                </div>
                <div class="w-[240px] h-[58px] bg-white rounded-[8px] flex flex-row justify-between cursor-pointer">
                    <div class="flex flex-row ml-5 ">
                        <img src="@/static/img/folder.svg" class="my-auto">
                        <div class=" leading-[58px] ml-4 font-normal truncate ">
                            Thành tích
                        </div>
                    </div>
                    <div class="flex flex-col my-auto mr-3">
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full mb-[3px]" />
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full mb-[3px]" />
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full" />
                    </div>
                </div>
                <div class="w-[240px] h-[58px] bg-white rounded-[8px] flex flex-row justify-between cursor-pointer">
                    <div class="flex flex-row ml-5 ">
                        <img src="@/static/img/folder.svg" class="my-auto">
                        <div class=" leading-[58px] ml-4 font-normal truncate ">
                            Thành tích
                        </div>
                    </div>
                    <div class="flex flex-col my-auto mr-3">
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full mb-[3px]" />
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full mb-[3px]" />
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full" />
                    </div>
                </div>
            </div>
        </div>
        <div class="text-[16px] font-bold mt-10 flex flex-col">
            <span class="mb-6">Sự kiện</span>
            <div class=" mb-6 w-[1032px] grid grid-cols-4 gap-4">
                <div class="w-[240px] h-[58px] bg-white rounded-[8px] flex flex-row justify-between cursor-pointer">
                    <div class="flex flex-row ml-5 ">
                        <img src="@/static/img/folder.svg" class="my-auto">
                        <div class=" leading-[58px] ml-4 font-normal truncate ">
                            Du lịch 2020
                        </div>
                    </div>
                    <div class="flex flex-col my-auto mr-3">
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full mb-[3px]" />
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full mb-[3px]" />
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full" />
                    </div>
                </div>
                <div class="w-[240px] h-[58px] bg-white rounded-[8px] flex flex-row justify-between cursor-pointer">
                    <div class="flex flex-row ml-5 ">
                        <img src="@/static/img/folder.svg" class="my-auto">
                        <div class=" leading-[58px] ml-4 font-normal truncate ">
                            Lễ khánh thành
                        </div>
                    </div>
                    <div class="flex flex-col my-auto mr-3">
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full mb-[3px]" />
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full mb-[3px]" />
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full" />
                    </div>
                </div>
                <div class="w-[240px] h-[58px] bg-white rounded-[8px] flex flex-row justify-between cursor-pointer">
                    <div class="flex flex-row ml-5 ">
                        <img src="@/static/img/folder.svg" class="my-auto">
                        <div class=" leading-[58px] ml-4 font-normal truncate ">
                            Khuyến học 2021
                        </div>
                    </div>
                    <div class="flex flex-col my-auto mr-3">
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full mb-[3px]" />
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full mb-[3px]" />
                        <div class="w-[3px] h-[3px] bg-gray-1 rounded-full" />
                    </div>
                </div>
            </div>
        </div>
        <div class="text-[16px] font-bold mt-10 flex flex-col">
            <span class="mb-6">Chung</span>
            <div class="w-[1032px] grid grid-cols-4 gap-4">
                <div class="h-[175px] w-[240px] flex flex-col cursor-pointer">
                    <img src="@/static/img/thumnail.png" class="w-full h-[135px]">
                    <div class="w-full h-10 bg-white flex flex-row">
                        <img src="@/static/img/file.svg" class="mr-3 my-auto ml-10">
                        <span class="text-[14px] leading-10">Điều lệ</span>
                    </div>
                </div>
                <div class="h-[175px] w-[240px] flex flex-col cursor-pointer">
                    <img src="@/static/img/thumnail.png" class="w-full h-[135px]">
                    <div class="w-full h-10 bg-white flex flex-row">
                        <img src="@/static/img/file.svg" class="mr-3 my-auto ml-10">
                        <span class="text-[14px] leading-10">Điều lệ</span>
                    </div>
                </div>
                <div class="h-[175px] w-[240px] flex flex-col cursor-pointer">
                    <img src="@/static/img/thumnail.png" class="w-full h-[135px]">
                    <div class="w-full h-10 bg-white flex flex-row">
                        <img src="@/static/img/file.svg" class="mr-3 my-auto ml-10">
                        <span class="text-[14px] leading-10">Điều lệ</span>
                    </div>
                </div>
                <div class="h-[175px] w-[240px] flex flex-col cursor-pointer">
                    <img src="@/static/img/thumnail.png" class="w-full h-[135px]">
                    <div class="w-full h-10 bg-white flex flex-row">
                        <img src="@/static/img/file.svg" class="mr-3 my-auto ml-10">
                        <span class="text-[14px] leading-10">Điều lệ</span>
                    </div>
                </div>
                <div class="h-[175px] w-[240px] flex flex-col cursor-pointer">
                    <img src="@/static/img/thumnail.png" class="w-full h-[135px]">
                    <div class="w-full h-10 bg-white flex flex-row">
                        <img src="@/static/img/file.svg" class="mr-3 my-auto ml-10">
                        <span class="text-[14px] leading-10">Điều lệ</span>
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
    }
</style>
