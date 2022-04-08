<template>
    <div class="flex flex-col bg-[#980C0F] h-max min-h-screen w-[240px] justify-between">
        <div class="flex flex-col">
            <div class="w-[160px] h-[160px] rounded-full mt-[170px] ml-[40px] avatar" />
            <div class="flex flex-col items-center mt-[24px] mb-[12px]">
                <img src="@/static/img/name.png" alt="">
            </div>
            <div class="flex flex-row justify-center mx-auto text-[#E79000] bg-[#FAE9CC] rounded-full w-[79px] h-[28px] leading-[28px]">
                Trưởng họ
            </div>
            <div class="flex justify-center text-[#ffffff] mt-[16px]">
                <span class="mx-auto">Đời thứ 8</span>
                <span class="mx-auto">27 tuổi</span>
            </div>
            <div class="mt-[16px] w-[189px] h-[34px] mx-auto rounded-[8px] bg-[#E79000] text-center leading-[34px] font-bold text-[16px]">
                Mã tài khoản: 168567
            </div>
            <div class="w-[240px] bg-[#CC4043] h-px mt-[24px]" />
            <div class="text-[#F5D399] mt-[32px] ml-[32px] mb-[24px] font-bold text-[16px]">
                <a href="#">Thông tin cá nhân</a>
            </div>
            <div class="text-[#ffffff] font-normal ml-[32px] text-[16px]">
                <a href="#">Thêm người thân</a>
            </div>
        </div>

        <div class="flex flex-col">
            <div class="mx-[32px] mb-[16px] font-normal text-[16px] text-[#fff]">
                <span class=" cursor-pointer" @click="repass()">Đổi mật khẩu</span>
            </div>
            <div>
                <button class="h-[48px] w-[181px] bg-[#E79000] text-[#ffffff] font-bold text-[18px] mx-[32px] mb-[32px]">
                    Đăng xuất
                </button>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        methods: {
            repass() {
                this.$router.push('/changepassword');
            },
        },
    };
</script>
<style scoped>
.avatar{
    background-image: url('@/static/img/avatar.jpeg');
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
}
</style>
