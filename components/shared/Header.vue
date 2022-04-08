<template>
    <div class="w-screen relative bg-[#FEF9F2]">
        <div class="bg-[#980C0F] bg-gray h-[72px] w-screen flex justify-around shadow-lg items-center z-100 absolute top-0">
            <div class="logo">
                <img src="@/static/img/logo.png">
            </div>
            <div class="flex flex-row">
                <div class="text-[16px] text-[#fff] font-normal ml-[20px] hover:text-[#F1BC66] hover:font-bold">
                    Sự kiện
                </div>
                <div class="group text-[16px] text-[#fff] font-normal ml-[20px] hover:text-[#F1BC66] hover:font-bold" @click="menuDown1()">
                    Thông tin dòng tộc <i class="el-icon-arrow-down" :class="{rotate1: isRotate1}" />
                    <div :class="{hover1: isHover1}" class="hidden absolute top-[80px] bg-[#980C0F] rounded-[4px] pt-[8px] pb-[8px] w-[180px]">
                        <a class="font-normal hover:bg-[#AD3D3F] pt-[8px] pl-[24px] pb-[8px] text-[#fff]">Cây gia phả</a>
                        <a class="font-normal hover:bg-[#AD3D3F] pt-[8px] pl-[24px] pb-[8px] text-[#fff]">Thông tin</a>
                        <a class="font-normal hover:bg-[#AD3D3F] pt-[8px] pl-[24px] pb-[8px] text-[#fff]">Ban liên lạc</a>
                        <a class="font-normal hover:bg-[#AD3D3F] pt-[8px] pl-[24px] pb-[8px] text-[#fff]">Tìm mộ phần</a>
                    </div>
                </div>

                <div class="text-[16px] text-[#fff] font-normal ml-[20px] hover:text-[#F1BC66] hover:font-bold">
                    Báo cáo
                </div>

                <div class="group text-[16px] text-[#fff] font-normal ml-[20px] hover:text-[#F1BC66] hover:font-bold" @click="menuDown2()">
                    Thư viện <i class="el-icon-arrow-down" :class="{rotate2: isRotate2}" />
                    <div :class="{hover2: isHover2}" class="hidden absolute top-[80px] bg-[#980C0F] rounded-[4px] pt-[8px] pb-[8px] w-[180px] ">
                        <a class=" font-normal hover:bg-[#AD3D3F] hover:font-bold pt-[8px] pl-[24px] pb-[8px] text-[#fff]">Thư viện ảnh</a>
                        <a class=" font-normal hover:bg-[#AD3D3F] hover:font-bold pt-[8px] pl-[24px] pb-[8px] text-[#fff]">Tài liệu</a>
                    </div>
                </div>

                <div class="text-[16px] text-[#fff] font-normal ml-[20px] hover:text-[#F1BC66] hover:font-bold">
                    Tin tức
                </div>
            </div>
            <div class="flex">
                <i class="el-icon-message-solid" />
                <div v-if="notAuth" class="flex">
                    <button class="w-[146px] h-[48px] bg-[#E79000] text-[#fff] text-[18px] font-bold my-auto rounded-[4px]">
                        Đăng nhập
                    </button>
                </div>
                <div v-else class="flex" @click="profile()">
                    <span class="text-[16px] font-bold text-[#fff] leading-[72px] mr-[16px]">Lê Văn Anh</span>
                    <div class="avatar w-[48px] h-[48px] rounded-full my-auto" />
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                id: 12,
                notAuth: false,
                isHover1: false,
                isHover2: false,
                isRotate1: false,
                isRotate2: false,
            };
        },
        methods: {
            menuDown1() {
                this.isHover1 = !this.isHover1;
                this.isRotate1 = !this.isRotate1;
                this.isHover2 = false;
                this.isRotate2 = false;
            },
            menuDown2() {
                this.isHover2 = !this.isHover2;
                this.isRotate2 = !this.isRotate2;
                this.isHover1 = false;
                this.isRotate1 = false;
            },
            profile() {
                this.$router.push(`/profile/${this.id}`);
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
    .el-icon-message-solid{
        color: #fff;
        font-size: 20px;
        line-height: 72px;
        margin-right: 43.25px;
    }
    .hover1{
        display: flex;
        flex-direction: column;
    }
    .hover2{
        display: flex;
        flex-direction: column;
    }
    .rotate1{
        transform: rotate(180deg);
    }
    .rotate2{
        transform: rotate(180deg);
    }
</style>
