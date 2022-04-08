<template>
    <div class="w-[1032px] mx-auto bg-[#fff] flex flex-col">
        <div v-if="!switchDialog" class="flex flex-row justify-around ">
            <div class="ml-[40px] mt-[40px] w-6/12">
                <img src="@/static/img/info.png" class="h-[38px]">
                <div class="mt-[16px] ">
                    <div class="flex flex-row">
                        <span class="text-[16px] text-[#252733] mr-[27px]">Bạn là con Dâu/Rể</span>
                        <el-switch v-model="switchDialog" active-color="#BF1014" />
                    </div>
                </div>
                <div class="mt-[25px]">
                    <span class="text-[16px]  text-[#252733]">Bạn là chồng hay vợ</span>
                    <div class="flex flex-row justify-between w-[410px] radiobtn">
                        <el-row class="radio-btn">
                            <div class="radio flex flex-row mr-[80px]" @click="gerderClick('husband')">
                                <div ref="husbandcircle" class="circle active">
                                    <div ref="husbandball" class="ball active" />
                                </div>
                                Chồng
                            </div>
                            <div class="radio flex flex-row mr-[80px]" @click="gerderClick('wife')">
                                <div ref="wifecircle" class="circle">
                                    <div ref="wifeball" class="ball " />
                                </div>
                                Vợ
                            </div>
                        </el-row>
                    </div>
                </div>
                <div v-for="item in listWife" :key="item" class="mt-[25px] mb-[8px]">
                    <span class="text-[16px] text-[#252733] ">Họ và tên Vợ</span>
                    <div class="mt-[8px] rounded-4 border h-[48px] border-[#FDF4E6] px-[16px] py-[11px] flex flex-row justify-between">
                        <span class="text-[16px] text-[#A3A4A9]">Chọn Vợ</span>
                        <i class="el-icon-arrow-up" />
                    </div>
                </div>
                <i class="el-icon-circle-plus" />
                <span class="text-[#E79000] text-[16px] ml-[18px] cursor-pointer" @click="addWife()">Thêm vợ</span>
                <div v-for="item in listChild" :key="item" class="mt-[25px] mb-[8px]">
                    <span class="text-[16px] text-[#252733] ">Họ và tên con</span>
                    <div class="mt-[8px] rounded-4 border h-[48px] border-[#FDF4E6] px-[16px] py-[11px] flex flex-row justify-between">
                        <span class="text-[16px] text-[#A3A4A9]">Chọn Con</span>
                        <i class="el-icon-arrow-up" />
                    </div>
                </div>
                <i class="el-icon-circle-plus" />
                <span class="text-[#E79000] text-[16px] ml-[18px] cursor-pointer" @click="addChild()">Thêm con</span>
                <div class="mt-[24px]">
                    <span class="text-[16px] text-[#1D1F2C]">Nếu người thân của bạn chưa có trong hệ thống, hãy thêm người thân, Admin sẽ kiểm tra và xét duyệt</span>
                </div>
                <div class="w-full mt-[9px]">
                    <button class="w-full h-[40px] rounded-[4px] border border-[#E79000]">
                        <i class="el-icon-circle-plus" />
                        <span class="text-[#E79000] text-[16px] mf-[18px]">Thêm người thân</span>
                    </button>
                </div>
            </div>
            <div class="ml-[40px] mt-[40px] w-6/12">
                <img src="@/static/img/info.png" class="h-[38px]">
                <div class="w-[456px] mr-[24px] mt-[16px] ">
                    <span class="text-[16px] text-[#252733] ">Họ và tên Bố đẻ</span>
                    <div class="mt-[8px] rounded-4 border h-[48px] border-[#FDF4E6] px-[16px] py-[11px] flex flex-row justify-between">
                        <span class="text-[16px] text-[#A3A4A9]">Chọn Bố</span>
                        <i class="el-icon-arrow-up" />
                    </div>
                </div>
                <div class="w-[456px] mr-[24px] mt-[24px] ">
                    <span class="text-[16px] text-[#252733] ">Họ và tên Mẹ đẻ</span>
                    <div class="mt-[8px] rounded-4 border h-[48px] border-[#FDF4E6] px-[16px] py-[11px] flex flex-row justify-between">
                        <span class="text-[16px] text-[#A3A4A9]">Chọn Mẹ</span>
                        <i class="el-icon-arrow-up" />
                    </div>
                </div>
                <img src="@/static/img/vigd.png" class="h-[38px] mt-[40px]">
                <div class="w-[456px] mr-[24px] mt-[24px] ">
                    <span class="text-[16px] text-[#252733] ">Con thứ</span>
                    <div class="mt-[8px] rounded-4 border h-[48px] border-[#FDF4E6] px-[16px] py-[11px] flex flex-row justify-between">
                        <span class="text-[16px] text-[#A3A4A9]">Chọn vị trí trong gia đình</span>
                        <i class="el-icon-arrow-up" />
                    </div>
                </div>
                <div class="mt-[8px] text-[14px] text-[#30323E]">
                    <span>Con thứ:</span>
                </div>
            </div>
        </div>
        <div v-else class="p-10">
            <img src="@/static/img/info.png" class="h-[38px]">
            <div class="mt-[16px] ">
                <div class="flex flex-row">
                    <span class="text-[16px] text-[#252733] mr-[27px]">Bạn là con Dâu/Rể</span>
                    <el-switch v-model="switchDialog" active-color="#BF1014" />
                </div>
            </div>
            <div class="mt-[25px]">
                <span class="text-[16px]  text-[#252733]">Bạn là chồng hay vợ</span>
                <div class="flex flex-row justify-between w-[410px] radiobtn">
                    <el-row class="radio-btn">
                        <div class="radio flex flex-row mr-[80px]" @click="gerderClick('husband')">
                            <div ref="husbandcircle" class="circle active">
                                <div ref="husbandball" class="ball active" />
                            </div>
                            Chồng
                        </div>
                        <div class="radio flex flex-row mr-[80px]" @click="gerderClick('wife')">
                            <div ref="wifecircle" class="circle">
                                <div ref="wifeball" class="ball " />
                            </div>
                            Vợ
                        </div>
                    </el-row>
                </div>
            </div>
            <div v-for="item in listWife" :key="item" class="mt-[25px] mb-[8px]">
                <span class="text-[16px] text-[#252733] ">Họ và tên Vợ</span>
                <div class="mt-[8px] rounded-4 border h-[48px] border-[#FDF4E6] px-[16px] py-[11px] flex flex-row justify-between">
                    <span class="text-[16px] text-[#A3A4A9]">Chọn Vợ</span>
                    <i class="el-icon-arrow-up" />
                </div>
            </div>
            <i class="el-icon-circle-plus" />
            <span class="text-[#E79000] text-[16px] ml-[18px] cursor-pointer" @click="addWife()">Thêm vợ</span>
            <div v-for="item in listChild" :key="item" class="mt-[25px] mb-[8px]">
                <span class="text-[16px] text-[#252733] ">Họ và tên con</span>
                <div class="mt-[8px] rounded-4 border h-[48px] border-[#FDF4E6] px-[16px] py-[11px] flex flex-row justify-between">
                    <span class="text-[16px] text-[#A3A4A9]">Chọn Con</span>
                    <i class="el-icon-arrow-up" />
                </div>
            </div>
            <i class="el-icon-circle-plus" />
            <span class="text-[#E79000] text-[16px] ml-[18px] cursor-pointer" @click="addChild()">Thêm con</span>
            <div class="mt-[24px]">
                <span class="text-[16px] text-[#1D1F2C]">Nếu người thân của bạn chưa có trong hệ thống, hãy thêm người thân, Admin sẽ kiểm tra và xét duyệt</span>
            </div>
            <div class="w-full mt-[9px]">
                <button class="w-full h-[40px] rounded-[4px] border border-[#E79000]">
                    <i class="el-icon-circle-plus" />
                    <span class="text-[#E79000] text-[16px] mf-[18px]">Thêm người thân</span>
                </button>
            </div>
            <img src="@/static/img/thongtingiadinh.png" class="mt-10">
            <div class="flex flex-row justify-between mt-4">
                <div class="w-[456px] mr-10 flex flex-col">
                    <div class=" font-bold text-[18px]">
                        <span>Bố đẻ</span>
                    </div>
                    <div class="mt-4 tetx-[16px]">
                        <span>Họ và tên Bố đẻ</span>
                    </div>
                    <div class="mt-2">
                        <SelectOption />
                    </div>
                    <div class="mt-4 text-[16px]">
                        <span>Ngày sinh</span>
                    </div>
                    <div class="mt-4">
                        <RadioButtons />
                    </div>
                    <div class="mt-4">
                        <el-date-picker
                            type="date"
                            placeholder="Ngày sinh dương lịch"
                        />
                    </div>
                    <div class="text-[14px] mt-4">
                        <span>Ngày sinh âm lịch: </span>
                    </div>
                    <div class="mt-4 text-[16px]">
                        <span>Số điện thoại</span>
                    </div>
                    <div class="mt-2">
                        <input type="text" class="px-4 py-3 rounded-[4px] border border-[#FDF4E6] w-full focus: outline-none" placeholder="Nhập số điện thoại">
                    </div>
                    <div class="mt-4 text-[16px]">
                        <span>Địa chỉ liên hệ</span>
                    </div>
                    <div class="mt-2">
                        <input type="text" class="px-4 py-3 rounded-[4px] border border-[#FDF4E6] w-full focus: outline-none" placeholder="Địa chỉ liên hệ">
                    </div>
                    <div class=" flex flex-row justify-between mt-4">
                        <span class="text-[16px]">Người thân đã qua đời</span>
                        <el-switch v-model="switchDialogDaddy" active-color="#BF1014" />
                    </div>
                    <div class="mt-4">
                        <RadioButtons />
                    </div>
                    <div class="mt-4">
                        <el-date-picker
                            type="date"
                            placeholder="Ngày mất dương lịch"
                        />
                    </div>
                    <div class="text-[14px] mt-4">
                        <span>Ngày mất âm lịch: </span>
                    </div>
                </div>
                <div class="w-[456px] flex flex-col">
                    <div class=" font-bold text-[18px]">
                        <span>Mẹ đẻ</span>
                    </div>
                    <div class="mt-4 tetx-[16px]">
                        <span>Họ và tên Mẹ đẻ</span>
                    </div>
                    <div class="mt-2">
                        <SelectOption />
                    </div>
                    <div class="mt-4 text-[16px]">
                        <span>Ngày sinh</span>
                    </div>
                    <div class="mt-4">
                        <RadioButtons />
                    </div>
                    <div class="mt-4">
                        <el-date-picker
                            type="date"
                            placeholder="Ngày sinh dương lịch"
                        />
                    </div>
                    <div class="text-[14px] mt-4">
                        <span>Ngày sinh âm lịch: </span>
                    </div>
                    <div class="mt-4 text-[16px]">
                        <span>Số điện thoại</span>
                    </div>
                    <div class="mt-2">
                        <input type="text" class="px-4 py-3 rounded-[4px] border border-[#FDF4E6] w-full focus: outline-none" placeholder="Nhập số điện thoại">
                    </div>
                    <div class="mt-4 text-[16px]">
                        <span>Địa chỉ liên hệ</span>
                    </div>
                    <div class="mt-2">
                        <input type="text" class="px-4 py-3 rounded-[4px] border border-[#FDF4E6] w-full focus: outline-none" placeholder="Địa chỉ liên hệ">
                    </div>
                    <div class=" flex flex-row justify-between mt-4">
                        <span class="text-[16px]">Người thân đã qua đời</span>
                        <el-switch v-model="switchDialogMomy" active-color="#BF1014" />
                    </div>
                    <div class="mt-4">
                        <RadioButtons />
                    </div>
                    <div class="mt-4">
                        <el-date-picker
                            type="date"
                            placeholder="Ngày mất dương lịch"
                        />
                    </div>
                    <div class="text-[14px] mt-4">
                        <span>Ngày mất âm lịch: </span>
                    </div>
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
    import RadioButtons from '@/components/UI/RadioButtons.vue';

    export default {
        components: {
            SelectOption,
            RadioButtons,
        },
        data() {
            return {
                switchDialog: true,
                gender: 'husband',
                listChild: [
                    {
                        id: 0,
                        name: '',
                    },
                ],
                listWife: [
                    {
                        id: 0,
                        name: '',
                    },
                ],
                iWife: 1,
                iChild: 1,
            };
        },
        methods: {
            gerderClick(gender) {
                this.gender = gender;
                if (this.gender === 'wife') {
                    this.$refs.wifecircle.classList.add('active');
                    this.$refs.wifeball.classList.add('active');
                    this.$refs.husbandcircle.classList.remove('active');
                    this.$refs.husbandball.classList.remove('active');
                } else if (this.gender === 'husband') {
                    this.$refs.wifecircle.classList.remove('active');
                    this.$refs.wifeball.classList.remove('active');
                    this.$refs.husbandcircle.classList.add('active');
                    this.$refs.husbandball.classList.add('active');
                }
            },
            addWife() {
                const newWife = {
                    id: this.iWife,
                    name: '',
                };
                this.listWife.push(newWife);
                this.iWife += 1;
            },
            addChild() {
                const newChild = {
                    id: this.iChild,
                    name: '',
                };
                this.listChild.push(newChild);
                this.iChild += 1;
            },
        },
    };
</script>
<style scoped>
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
    }
    .circle.active{
        border: 2px solid #BF1014;
    }
    .ball.active{
        display: block;

    }
    .radiobtn{
        margin-top: 16px;
    }
    .el-icon-arrow-up{
        color: #75767E;
        margin: auto 0;
    }
    .el-icon-circle-plus{
        font-size: 20px;
        color: #E79000;
    }
    .el-date-editor.el-input.el-input--prefix.el-input--suffix.el-date-editor--date{
        width: 456px;
        height: 48px;
    }
</style>
