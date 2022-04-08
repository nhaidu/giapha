<template>
    <div class="flex flex-col w-[592px] bg-[#FDF4E6] py-6 px-10 rounded-[4px]">
        <div class="text-[#1D1F2C]">
            <span class="text-[16px] mr-2">Tổng thu</span>
            <span class="text-[24px] font-bold">3.000.000.000 đ</span>
        </div>
        <div v-for="i in 40" :key="i">
            <div v-if="i % 2 === 0 " class="bg-white mt-2 w-[513px] h-[134px] p-6 flex flex-row justify-between rounded-[4px]">
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
                <div class="flex flex-col text-right">
                    <span class="text-[#08B04F] text-[18px] ">+ 7.000.000 đ</span>
                    <div class="flex flex-row justify-between">
                        <div />
                        <div class="w-[100px] h-[28px] text-center rounded-full bg-[#D6E7FB] text-[12px] text-[#369FFF] mt-2">
                            <span class=" leading-[28px]">Chuyển khoản</span>
                        </div>
                    </div>
                    <div class=" flex flex-row mt-2 mr-0">
                        <i class="el-icon-time" />
                        <span class="ml-2 text-[#75767E] text-[14px]">12:30 - 12/12/2021</span>
                    </div>
                </div>
            </div>
            <div v-else class="bg-white mt-2 w-[513px] h-[134px] p-6 flex flex-row justify-between rounded-[4px]">
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
                <div class="flex flex-col relative mr-0 text-right">
                    <span class="text-[#08B04F] text-[18px] mr-0 ">+ 7.000.000 đ</span>
                    <div class="flex flex-row justify-between">
                        <div />
                        <div class="w-[100px] h-[28px] text-center rounded-full bg-[#FDF5D8] text-[12px] text-[#FF9900] mt-2 mr-0">
                            <span class=" leading-[28px]">Tiền mặt</span>
                        </div>
                    </div>
                    <div class=" flex flex-row mt-2 mr-0">
                        <i class="el-icon-time" />
                        <span class="ml-2 text-[#75767E] text-[14px]">12:30 - 12/12/2021</span>
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
    .el-icon-phone, .el-icon-message{
        color: #E79000;
        margin: auto 0;
        margin-right: 8px;
    }
    .el-icon-time{
        color: #BF1014;
    }
</style>
