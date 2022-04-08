<template>
    <div class="w-[768px] h-[728px] bg-white flex flex-col px-10 py-10 rounded-[20px] mb-[90px]">
        <div class="flex flex-row justify-between mb-[25px]">
            <div>
                <img src="@/static/img/ttcn.png" class="h-[38px] w-[154px] py-auto">
            </div>
            <div class="py-auto my-auto">
                <img src="@/static/img/pen.png" class="h-[20px] w-[20px]">
            </div>
        </div>
        <div class="flex flex-row mb-4">
            <div class="h-[26px] w-[130px] font-bold text-[#252733] text-[16px] leading-[26px]">
                <span>Giới tính</span>
            </div>
            <div class="text-[16px] text-[#252733] leading-[26px]">
                Nam
            </div>
        </div>
        <div class="flex flex-row mb-4">
            <div class="h-[26px] w-[130px] font-bold text-[#252733] text-[16px] leading-[26px]">
                <span>Ngày sinh</span>
            </div>
            <div class="flex flex-col text-[16px] text-[#252733] leading-[26px]">
                <span>20/10/1986(DL)</span>
                <span>08/09/1986(AL)</span>
            </div>
        </div>
        <div class="flex flex-row mb-4">
            <div class="h-[26px] w-[130px] font-bold text-[#252733] text-[16px] leading-[26px]">
                <span>Nguyên quán</span>
            </div>
            <div class="text-[16px] text-[#252733] leading-[26px]">
                <span>Phương Mai, Đông Đa, Hà Nội</span>
            </div>
        </div>
        <div class="flex flex-row mb-4">
            <div class="h-[26px] w-[130px] font-bold text-[#252733] text-[16px] leading-[26px]">
                <span>Nơi sinh</span>
            </div>
            <div class="text-[16px] text-[#252733] leading-[26px]">
                <span>Phương Mai, Đống Đa, Hà Nội</span>
            </div>
        </div>
        <div class="flex flex-row mb-10">
            <div class="h-[26px] w-[130px] font-bold text-[#252733] text-[16px] leading-[26px]">
                <span>Quốc tịch</span>
            </div>
            <div class="text-[16px] text-[#252733] leading-[26px]">
                <span>Việt Nam</span>
            </div>
        </div>
        <div class="py-auto mb-6">
            <img src="@/static/img/ttlh.png" class="h-[38px] w-[143px]">
        </div>
        <div class=" h-[26px] mb-4">
            <i class="el-icon-phone" />
            <span class="ml-[18px] leading-[26px] text-[16px]">0986 768 968</span>
        </div>
        <div class=" h-[26px] mb-4">
            <i class="el-icon-message" />
            <span class="ml-[18px] leading-[26px] text-[16px]">anhle8896@gmail.com</span>
        </div>
        <div class=" h-[26px] mb-10">
            <i class="el-icon-location-outline" />
            <span class="ml-[18px] leading-[26px] text-[16px]">86 Phương Mai, Đống Đa, Hà Nội</span>
        </div>
        <div class="py-auto mb-6">
            <img src="@/static/img/mxh.png" class="h-[38px] w-[143px]">
        </div>
        <div class=" h-[26px] mb-4 flex flex-row">
            <img src="@/static/img/zalo.png">
            <span class="ml-[18px] leading-[26px] text-[16px]">0986 768 968</span>
        </div>
        <div class=" h-[26px] mb-10 flex flex-row">
            <div class=" leading-[26px]">
                <img src="@/static/img/fb.png">
            </div>
            <span class="ml-[18px] leading-[26px] text-[16px]">anhle@facebook.com</span>
        </div>
    </div>
</template>
<script>
    export default {
        methods: {

        },
    };
</script>
<style scoped>
    .el-icon-edit{
        font-size: 20px;
    }
    .el-icon-phone, .el-icon-location-outline, .el-icon-message{
        color: #BF1014;
        font-size: 20px;
        line-height: 26px;
    }
</style>
