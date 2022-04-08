<template>
    <div class="flex flex-col w-[592px] bg-[#FDF4E6] py-6 px-10 rounded-[4px]">
        <div v-for="i in 40" :key="i">
            <div class="bg-white mt-2 w-[513px] h-[134px] p-6 flex flex-row rounded-[4px]">
                <div class="flex flex-row">
                    <div class="w-[80px] h-[80px] rounded-full bg-pink-400 my-auto mr-4" />
                    <div class="flex flex-col">
                        <span class="text-[16px] font-bold">Lê Văn Anh</span>
                        <div class="flex flex-row">
                            <i class="el-icon-phone" />
                            <span class="text-[#75767E] text-[14px] ml-2">0986 768 968</span>
                        </div>
                        <div class="flex flex-row">
                            <i class="el-icon-message" />
                            <span class="text-[#75767E] text-[14px] ml-2">anhle8896@gmail.com</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style>
    .el-icon-phone, .el-icon-message{
        color: #E79000;
        margin: auto 0;
        margin-right: 8px;
    }
</style>
