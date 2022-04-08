<template>
    <div class=" relative bg-[#FEF9F2] flex flex-col ">
        <div class="flex flex-row justify-items-start mb-[24px] w-[1032px] mx-auto">
            <div class="inline-block">
                <span class="text-[16px] text-[#606266] mr-[13px]">Trang chủ</span>
                <i class="el-icon-arrow-right" />
                <span class="text-[16px] text-[#606266] mr-[13px]">Cá nhân</span>
                <i class="el-icon-arrow-right" />
                <span class="text-[16px] text-[#606266] mr-[13px]">Thông tin cá nhân</span>
                <i class="el-icon-arrow-right" />
                <span class="text-[16px] text-[#606266] font-bold">Lê Văn Anh</span>
            </div>
        </div>
        <div class="flex flex-col justify-items-start w-[856px] mx-auto">
            <div>
                <span class="text-[24px] text-[#1D1F2C] font-bold">Nguyễn Văn Thành</span>
            </div>
            <div class="mt-2 text-[16px] text-[#75767E]">
                <span>Bố đẻ của: Nguyễn Thị Đào</span>
            </div>
            <div class="mt-2 text-[16px] text-[#75767E]">
                <span>Bố vợ thứ nhất của: Lê Văn Anh</span>
            </div>
        </div>
        <div class="mt-10 flex flex-col justify-items-start w-[856px] mx-auto bg-white mb-[208px] p-10 rounded-[20px]">
            <img src="@/static/img/toittcn.png" class="h-[38px] w-[154px]">
            <div class="flex flex-row mt-4">
                <div class="w-[130px] text-[16px] text-[#252733]">
                    <span class="font-bold">Giới tính</span>
                </div>
                <div>
                    <span>Nam</span>
                </div>
            </div>
            <div class="flex flex-row mt-4">
                <div class="w-[130px] text-[16px] text-[#252733]">
                    <span class="font-bold">Ngày sinh</span>
                </div>
                <div>
                    <div class="mt-2">
                        <span>20/10/1986 (DL)</span>
                    </div>
                    <div class="mt-2">
                        <span>08/09/1986 (AL)</span>
                    </div>
                </div>
            </div>
            <div class="flex flex-row mt-4">
                <div class="w-[130px] text-[16px] text-[#252733]">
                    <span class="font-bold">Ngày mất</span>
                </div>
                <div>
                    <div class="mt-2">
                        <span>20/10/1986 (DL)</span>
                    </div>
                    <div class="mt-2">
                        <span>08/09/1986 (AL)</span>
                    </div>
                </div>
            </div>
            <img src="@/static/img/toittln.png" class="mt-10 h-[38px] w-[143px]">
            <div class="flex flex-row mt-4">
                <div class="mr-4 text-[20px] text-[#BF1014]">
                    <i class="el-icon-phone" />
                </div>
                <div class="text-[16px] text-[#191B28]">
                    <span>0986 768 968</span>
                </div>
            </div>
            <div class="flex flex-row mt-4">
                <div class="mr-4 text-[20px] text-[#BF1014]">
                    <i class="el-icon-message" />
                </div>
                <div class="text-[16px] text-[#191B28]">
                    <span>anhle8896@gmail.com</span>
                </div>
            </div>
            <div class="flex flex-row mt-4">
                <div class="mr-4 text-[20px] text-[#BF1014]">
                    <i class="el-icon-location" />
                </div>
                <div class="text-[16px] text-[#191B28]">
                    <span>86 Phương Mai, Đống Đa, Hà Nội</span>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default {

    };
</script>
<style scoped>
    .el-icon-arrow-right{
        margin-right: 13px;
    }
</style>
