<template>
    <div class="w-[1032px] mx-auto flex flex-col">
        <div class="w-[1032px] flex flex-row justify-items-start mb-[24px]">
            <div class="inline-block">
                <span class="text-[16px] text-[#606266] mr-[13px]">Trang chủ</span>
                <i class="el-icon-arrow-right mr-[13px]" />
                <span class="text-[16px] text-[#606266] mr-[13px]">Thống kê</span>
                <i class="el-icon-arrow-right mr-[13px]" />
                <span class="text-[16px] text-[#606266] font-bold">Nhân số</span>
            </div>
        </div>
        <div class="flex flex-row mt-6">
            <div class="flex flex-col w-[240px] mr-6">
                <span class="text-[#252733] text-[36px] font-bold mb-5">Thành viên</span>
                <div class="w-[240px] mr-6 mb-[18px]">
                    <CheckBox :check-box-data="checkBoxData1" :title="'Tình trạng'" @checkedBox="checkedBox1($event)" />
                </div>
                <div class="w-full border border-[#FAE9CC] mb-[18px]" />
                <div class="w-[240px] mr-6 mb-[18px]">
                    <CheckBox :check-box-data="checkBoxDataGender" :title="'Giới tính'" @checkedBox="checkedBoxGender($event)" />
                </div>
                <div class="w-full border border-[#FAE9CC] mb-[18px]" />
                <div class="w-[240px] mr-6 mb-[18px]">
                    <CheckBox :check-box-data="checkBoxDataOld" :title="'Độ tuổi'" @checkedBox="checkedBoxOld($event)" />
                </div>
                <div class="w-full border border-[#FAE9CC] mb-[18px]" />
                <div class="w-[240px] mr-6 mb-[18px]">
                    <CheckBox :check-box-data="checkBoxData2" :title="'Dâu / Rể'" @checkedBox="checkedBox2($event)" />
                </div>
            </div>
            <div class="w-[768px] flex flex-col">
                <div>
                    <el-input
                        v-model="input"
                        placeholder="Nhập tên để tìm kiếm"
                        suffix-icon="el-icon-search"
                    />
                </div>
                <div class="mt-[28px]">
                    <span class="text-[16px] text-[#1D1F2C]"> Tổng cộng: 1.200 thành viên </span>
                </div>
                <div class="mt-4 flex flex-row flex-wrap">
                    <div v-for="item in value" :key="item" class="mr-2 mt-1">
                        <div class="px-4 py-2 flex flex-row bg-[#F9E8E8] text-[#BF1014] text-[14px] rounded-full">
                            <span class="mr-3"> {{ item.name }} </span>
                            <img src="@/static/img/daux.svg" @click="removeFilter(item.id, item.option, item.idOption)">
                        </div>
                    </div>
                </div>
                <div class="mt-4 flex flex-row justify-between flex-wrap">
                    <div v-for="item in 15" :key="item" class="mb-4">
                        <div class="w-[240px] h-[244px] bg-white shadow-lg rounded-[4px] flex flex-col p-4">
                            <div class="w-[80px] h-[80px] rounded-full bg-violet-6 mx-auto" />
                            <div class="mt-4 mx-auto">
                                <span class="text-[16px] font-bold">Lê Văn Anh</span>
                            </div>
                            <div class="mt-1 text-[#75767E] text-[14px] mx-auto">
                                Đời thứ 8 - Chi thứ 1
                            </div>
                            <div class="mt-4 flex flex-row">
                                <div class="mr-2 text-[14px] text-[#E79000]">
                                    <i class="el-icon-phone" />
                                </div>
                                <div class="text-[#75767E] text-[14px]">
                                    0986 768 968
                                </div>
                            </div>
                            <div class="mt-1 flex flex-row">
                                <div class="mr-2 text-[14px] text-[#E79000]">
                                    <i class="el-icon-message" />
                                </div>
                                <div class="text-[#75767E] text-[14px]">
                                    anhle8896@gmail.com
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import CheckBox from '@/components/UI/CheckBox.vue';

    export default {
        components: {
            CheckBox,
        },
        data() {
            return {
                input: null,
                checkBoxData1: [
                    {
                        id: 0,
                        name: 'Còn sống',
                        chose: false,
                    },
                    {
                        id: 1,
                        name: 'Đã mất',
                        chose: false,
                    },
                ],
                checkBoxData2: [
                    {
                        id: 0,
                        name: 'Con Dâu',
                        chose: false,
                    },
                    {
                        id: 1,
                        name: 'Con Rể',
                        chose: false,
                    },
                ],
                checkBoxDataGender: [
                    {
                        id: 0,
                        name: 'Nam',
                        chose: false,
                    },
                    {
                        id: 1,
                        name: 'Nữ',
                        chose: false,
                    },
                    {
                        id: 2,
                        name: 'Khác',
                        chose: false,
                    },
                ],
                checkBoxDataOld: [
                    {
                        id: 0,
                        name: '>=100',
                        chose: false,
                    },
                    {
                        id: 1,
                        name: '90-99',
                        chose: false,
                    },
                    {
                        id: 2,
                        name: '80-89',
                        chose: false,
                    },
                    {
                        id: 3,
                        name: '70-79',
                        chose: false,
                    },
                    {
                        id: 4,
                        name: '60-69',
                        chose: false,
                    },
                    {
                        id: 5,
                        name: '40-59',
                        chose: false,
                    },
                    {
                        id: 6,
                        name: '18-39',
                        chose: false,
                    },
                    {
                        id: 7,
                        name: '6-17',
                        chose: false,
                    },
                    {
                        id: 8,
                        name: '0-5',
                        chose: false,
                    },
                ],
                value: [
                ],
                i: 0,
            };
        },
        methods: {
            checkedBox1($event) {
                this.checkBoxData1[$event].chose = !this.checkBoxData1[$event].chose;
                if (this.checkBoxData1[$event].chose === true) {
                    const temp = {
                        id: this.i,
                        idOption: this.checkBoxData1[$event].id,
                        name: this.checkBoxData1[$event].name,
                        option: 'checkBoxData1',
                    };
                    this.value.push(temp);
                    this.i += 1;
                } else {
                    this.value = this.value.filter((item) => item.name !== this.checkBoxData1[$event].name);
                }
            },
            checkedBoxGender($event) {
                this.checkBoxDataGender[$event].chose = !this.checkBoxDataGender[$event].chose;
                if (this.checkBoxDataGender[$event].chose === true) {
                    const temp = {
                        id: this.i,
                        idOption: this.checkBoxDataGender[$event].id,
                        name: this.checkBoxDataGender[$event].name,
                        option: 'checkBoxDataGender',
                    };
                    this.value.push(temp);
                    this.i += 1;
                } else {
                    this.value = this.value.filter((item) => item.name !== this.checkBoxDataGender[$event].name);
                }
            },
            checkedBoxOld($event) {
                this.checkBoxDataOld[$event].chose = !this.checkBoxDataOld[$event].chose;
                if (this.checkBoxDataOld[$event].chose === true) {
                    const temp = {
                        id: this.i,
                        idOption: this.checkBoxDataOld[$event].id,
                        name: this.checkBoxDataOld[$event].name,
                        option: 'checkBoxDataOld',
                    };
                    this.value.push(temp);
                    this.i += 1;
                } else {
                    this.value = this.value.filter((item) => item.name !== this.checkBoxDataOld[$event].name);
                }
            },
            checkedBox2($event) {
                this.checkBoxData2[$event].chose = !this.checkBoxData2[$event].chose;
                if (this.checkBoxData2[$event].chose === true) {
                    const temp = {
                        id: this.i,
                        idOption: this.checkBoxData2[$event].id,
                        name: this.checkBoxData2[$event].name,
                        option: 'checkBoxData2',
                    };
                    this.value.push(temp);
                    this.i += 1;
                } else {
                    this.value = this.value.filter((item) => item !== this.checkBoxData2[$event].name);
                }
            },
            removeFilter(param1, param2, param3) {
                this.value = this.value.filter((item) => item.id !== param1);
                if (param2 === 'checkBoxData1') {
                    this.checkBoxData1[param3].chose = false;
                } else if (param2 === 'checkBoxData2') {
                    this.checkBoxData2[param3].chose = false;
                } else if (param2 === 'checkBoxDataGender') {
                    this.checkBoxDataGender[param3].chose = false;
                } else if (param2 === 'checkBoxDataOld') {
                    this.checkBoxDataOld[param3].chose = false;
                }
            },
        },
    };
</script>
<style>
    input.el-input__inner {
        height: 48px;
    }
</style>
