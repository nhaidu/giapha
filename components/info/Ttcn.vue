<template>
    <div class="w-[1032px] mx-auto bg-[#fff] flex flex-col">
        <div class="flex flex-row justify-around">
            <div class="ml-[40px] mt-[40px]">
                <div class="flex flex-col">
                    <div class="upload-btn-wrapper mt-[16px]">
                        <button class="btn">
                            <i class="el-icon-camera-solid" />
                        </button>
                        <el-upload
                            class="avatar-uploader"
                            action="https://jsonplaceholder.typicode.com/posts/"
                            :show-file-list="false"
                            :on-success="handleAvatarSuccess"
                            :before-upload="beforeAvatarUpload"
                        >
                            <img v-if="imageUrl" :src="imageUrl" class="avatar w-[153px] h-[153px]">
                            <i v-else class="el-icon-plus avatar-uploader-icon" />
                        </el-upload>
                    </div>
                    <span class="text-[16px]  text-[#30323E] mb-[16px] w-[140px] text-center">Đổi avatar</span>
                </div>
                <div class="flex flex-col">
                    <span class="text-[16px]  text-[#252733] mb-[8px]">Họ và tên</span>
                    <input type="text" placeholder="Họ và tên" class="placeholder:text-[16px] mb-[24px] focus:bg-[#FAE9CC] w-[456px] h-[48px] border border-[#FDF4E6] pl-[16px]">
                </div>
                <div class="flex flex-col">
                    <span class="text-[16px]  text-[#252733] mb-[8px]">Tên thường gọi</span>
                    <input type="text" placeholder="Tên thường gọi" class="placeholder:text-[16px] mb-[24px] focus:bg-[#FAE9CC] w-[456px] h-[48px] border border-[#FDF4E6] pl-[16px]">
                </div>
                <div class="flex flex-col">
                    <span class="text-[16px]  text-[#252733] mb-[8px]">Nguyên quán</span>
                    <input type="text" placeholder="Nhập nguyên quán" class="placeholder:text-[16px] mb-[24px] focus:bg-[#FAE9CC] w-[456px] h-[48px] border border-[#FDF4E6] pl-[16px]">
                </div>
                <div class="flex flex-col">
                    <span class="text-[16px]  text-[#252733] mb-[8px]">Nơi sinh</span>
                    <input type="text" placeholder="Nhập nơi sinh" class="placeholder:text-[16px] mb-[24px] focus:bg-[#FAE9CC] w-[456px] h-[48px] border border-[#FDF4E6] pl-[16px]">
                </div>
                <div class="flex flex-col">
                    <span class="text-[16px]  text-[#252733] mb-[8px]">Quốc tịch</span>
                    <input type="text" placeholder="Nhập quốc tịch" class="placeholder:text-[16px] mb-[24px] focus:bg-[#FAE9CC] w-[456px] h-[48px] border border-[#FDF4E6] pl-[16px]">
                </div>
                <div class="flex flex-col">
                    <span class="text-[16px]  text-[#252733] mb-[8px]">Giới tính</span>
                    <div class="flex flex-row justify-between w-[410px] mb-[16px]">
                        <el-row class="radio-btn">
                            <div class="radio flex flex-row mr-[80px]" @click="radioClick('nam')">
                                <div ref="gendercircle1" class="circle active">
                                    <div ref="genderball1" class="ball active" />
                                </div>
                                Nam
                            </div>
                            <div class="radio flex flex-row mr-[80px]" @click="radioClick('nu')">
                                <div ref="gendercircle2" class="circle">
                                    <div ref="genderball2" class="ball" />
                                </div>
                                Nữ
                            </div>
                            <div class="radio flex flex-row mr-[80px]" @click="radioClick('bd')">
                                <div ref="gendercircle3" class="circle">
                                    <div ref="genderball3" class="ball " />
                                </div>
                                Khác
                            </div>
                        </el-row>
                    </div>
                </div>
                <div class="flex flex-col">
                    <span class="text-[16px]  text-[#252733] mb-[8px]">Ngày sinh</span>
                    <div class="flex flex-row justify-left w-[410px]">
                        <el-row class="radio-btn">
                            <div class="radio flex flex-row mr-[40px]" @click="radioClick('duong')">
                                <div ref="datecircle1" class="circle active">
                                    <div ref="dateball1" class="ball active" />
                                </div>
                                Ngày dương lịch
                            </div>
                            <div class="radio flex flex-row mr-[40px]" @click="radioClick('am')">
                                <div ref="datecircle2" class="circle ">
                                    <div ref="dateball2" class="ball " />
                                </div>
                                Ngày âm lịch
                            </div>
                        </el-row>
                    </div>
                    <div>
                        <el-date-picker
                            v-model="date"
                            type="dates"
                            placeholder="Ngày sinh dương lịch"
                        />
                    </div>
                </div>
                <div class="mt-[24px] text-[14px] text-[#30323E]">
                    <span>Ngày sinh âm lịch:</span>
                </div>
            </div>
            <div class="">
                <div class="flex flex-col mt-[40px]">
                    <img src="@/static/img/contact.png" class="w-[153px] h-[38px]">
                </div>
                <div class="flex flex-col mt-[16px]">
                    <span class="text-[16px]  text-[#252733] mb-[8px]">Số điện thoại</span>
                    <input type="text" placeholder="Nhập số điện thoại" class="placeholder:text-[16px] mb-[24px] focus:bg-[#FAE9CC] w-[456px] h-[48px] border border-[#FDF4E6] pl-[16px]">
                </div>
                <div class="flex flex-col">
                    <span class="text-[16px]  text-[#252733] mb-[8px]">Email</span>
                    <input type="text" placeholder="Nhập email" class="placeholder:text-[16px] mb-[24px] focus:bg-[#FAE9CC] w-[456px] h-[48px] border border-[#FDF4E6] pl-[16px]">
                </div>
                <div class="flex flex-col">
                    <span class="text-[16px]  text-[#252733] mb-[8px]">Facebook</span>
                    <input type="text" placeholder="Nhập link facebook" class="placeholder:text-[16px] mb-[24px] focus:bg-[#FAE9CC] w-[456px] h-[48px] border border-[#FDF4E6] pl-[16px]">
                </div>
                <div class="flex flex-col">
                    <span class="text-[16px]  text-[#252733] mb-[8px]">Zalo</span>
                    <input type="text" placeholder="Nhập link Zalo/Số điện thoại dùng Zalo" class="mb-[24px] focus:bg-[#FAE9CC] w-[456px] h-[48px] border border-[#FDF4E6] pl-[16px]">
                </div>
                <div class="flex flex-col mt-[40px]">
                    <img src="@/static/img/address.png" class="w-[153px] h-[38px]">
                </div>
                <div class="flex flex-row mt-[16px]">
                    <div class="w-[216px] mr-[24px]">
                        <span class="text-[16px] text-[#252733] ">Tỉnh/TP</span>
                        <SelectOption />
                    </div>
                    <div class="w-[216px]">
                        <span class="text-[16px] text-[#252733] ">Quận/Huyện</span>
                        <div class=" mt-[8px] rounded-4 border h-[48px] border-[#FDF4E6] px-[16px] py-[11px] flex flex-row justify-between">
                            <span class="text-[16px] text-[#A3A4A9]">Chọn Quận/Huyện</span>
                            <i class="el-icon-arrow-up" />
                        </div>
                    </div>
                </div>
                <div>
                    <div class="w-[456px] mr-[24px] mt-[16px] ">
                        <span class="text-[16px] text-[#252733] ">Phường/Xã</span>
                        <div class="mt-[8px] rounded-4 border h-[48px] border-[#FDF4E6] px-[16px] py-[11px] flex flex-row justify-between">
                            <span class="text-[16px] text-[#A3A4A9]">Chọn Phường/Xã</span>
                            <i class="el-icon-arrow-up" />
                        </div>
                    </div>
                </div>
                <div class="flex flex-col">
                    <span class="text-[16px] mt-[16px] text-[#252733] mb-[8px]">Địa chỉ cụ thể</span>
                    <input type="text" placeholder="Nhập địa chỉ" class="mb-[24px] focus:bg-[#FAE9CC] w-[456px] h-[48px] border border-[#FDF4E6] pl-[16px]">
                </div>
            </div>
        </div>

        <button class="mx-auto mb-[40px] bg-[#A3A4A9] rounded-[4px] text-[#fff] w-[382px] h-[48px] mt-[40px] text-[18px] font-bold leading-[48px]">
            Lưu thông tin
        </button>
    </div>
</template>
<script>
    import SelectOption from '@/components/UI/SelectOption.vue';

    export default {
        components: {
            SelectOption,
        },
        data() {
            return {
                typedate: 'duong',
                date: '',
                gender: 'nam',
                imageUrl: '@/static/img/info.png',
            };
        },
        methods: {
            handleAvatarSuccess(res, file) {
                this.imageUrl = '';
                this.imageUrl = URL.createObjectURL(file.raw);
            },
            beforeAvatarUpload(file) {
                const isJPG = file.type === 'image/jpeg';
                const isLt2M = file.size / 1024 / 1024 < 2;

                if (!isJPG) {
                    this.$message.error('Avatar picture must be JPG format!');
                }
                if (!isLt2M) {
                    this.$message.error('Avatar picture size can not exceed 2MB!');
                }
                return isJPG && isLt2M;
            },
            radioClick(param) {
                if (param === 'am') {
                    this.typedate = param;
                    this.$refs.datecircle2.classList.add('active');
                    this.$refs.dateball2.classList.add('active');
                    this.$refs.datecircle1.classList.remove('active');
                    this.$refs.dateball1.classList.remove('active');
                } else if (param === 'duong') {
                    this.typedate = param;
                    this.$refs.datecircle2.classList.remove('active');
                    this.$refs.dateball2.classList.remove('active');
                    this.$refs.datecircle1.classList.add('active');
                    this.$refs.dateball1.classList.add('active');
                } else if (param === 'nam') {
                    this.gender = param;
                    this.$refs.gendercircle3.classList.remove('active');
                    this.$refs.genderball3.classList.remove('active');
                    this.$refs.gendercircle2.classList.remove('active');
                    this.$refs.genderball2.classList.remove('active');
                    this.$refs.gendercircle1.classList.add('active');
                    this.$refs.genderball1.classList.add('active');
                } else if (param === 'nu') {
                    this.gender = param;
                    this.$refs.gendercircle3.classList.remove('active');
                    this.$refs.genderball3.classList.remove('active');
                    this.$refs.gendercircle2.classList.add('active');
                    this.$refs.genderball2.classList.add('active');
                    this.$refs.gendercircle1.classList.remove('active');
                    this.$refs.genderball1.classList.remove('active');
                } else if (param === 'bd') {
                    this.gender = param;
                    this.$refs.gendercircle3.classList.add('active');
                    this.$refs.genderball3.classList.add('active');
                    this.$refs.gendercircle2.classList.remove('active');
                    this.$refs.genderball2.classList.remove('active');
                    this.$refs.gendercircle1.classList.remove('active');
                    this.$refs.genderball1.classList.remove('active');
                }
            },
        },
    };
</script>
<style scoped>
    *:focus {
        outline: none;
    }
    .avatar-uploader{
        width: 153px;
        height: 153px;
    }
    .upload-btn-wrapper {
    position: relative;
    overflow: hidden;
    display: inline-block;
    background-image: url('@/static/img/avatar.jpeg');
    width: 152px;
    height: 152px;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    border-radius: 1000px;
    position: relative;
    }

    .btn {
    color: white;
    background: rgba(25, 27, 40, 0.5);
    padding: 8px 20px;
    width: 160px;
    height: 40px;
    font-size: 20px;
    position: absolute;
    bottom:0;
    }

    .upload-btn-wrapper input[type=file] {
    font-size: 100px;
    position: absolute;
    left: 0;
    top: 0;
    opacity: 0;
    }
    .el-date-picker{
        width: 456px;
    }
    .radio-btn{
        display: flex;
        justify-content: center;
        color: #30323E;
        font-size: 16px;
        font-weight: 400;
        margin-bottom: 16px;
    }
    .circle{
        margin-right: 16px;
        width: 24px;
        height: 24px;
        border: 2px solid #BABBBE;
        border-radius: 50px;
        position: relative;
        background-color: #ffffff;
    }
    .ball{
        display: none;
        width: 14px;
        height: 14px;
        background-color: #BF1014;
        border-radius: 50px;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }.circle.active{
        border: 2px solid #BF1014;
    }
    .ball.active{
        display: block;

    }
    .el-icon-arrow-up{
        color: #75767E;
        margin: auto 0;
    }
    input[type='radio']:checked{
        color: red;
    }
    .el-date-editor.el-input.el-input--prefix.el-input--suffix.el-date-editor--date{
        width: 100%;
        height: 48px;
    }
</style>
