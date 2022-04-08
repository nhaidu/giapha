<template>
    <div class="w-[1032px] mx-auto bg-[#fff] flex flex-col">
        <div class="flex flex-row justify-around">
            <div class="ml-[40px] mt-[40px] w-6/12">
                <img src="@/static/img/class.png">
                <div class="flex flex-row mt-[16px]">
                    <div class="w-[216px] mr-[24px]">
                        <span class="text-[16px] text-[#252733] ">Chọn trình độ cao nhất</span>
                        <SelectOption />
                    </div>
                    <div class="w-[216px]">
                        <span class="text-[16px] text-[#252733] ">Chọn lớp học hiện tại</span>
                        <SelectOption />
                    </div>
                </div>
                <img src="@/static/img/vector.png" class="mt-[16px] mb-[16px]">
                <span class="text-[16px] text-[#252733] ">Thành tích</span>
                <div v-for="item in listAchievement" :key="item">
                    <img v-if="item !== listAchievement[0]" src="@/static/img/vector.png" class="mb-[16px] mt-[12px]">
                    <div class="flex flex-row mt-[12px]">
                        <div class="w-[216px] mr-[24px]">
                            <span class="text-[16px] text-[#252733] ">Lớp học</span>
                            <SelectOption />
                        </div>
                        <div class="w-[216px]">
                            <span class="text-[16px] text-[#252733] ">Trình độ học tập</span>
                            <SelectOption />
                        </div>
                    </div>
                    <div class="mt-[8px]">
                        <button class="w-[456px] h-[48px] text-[#E79000] text-[16px] bg-[#FDF4E6] text-center " @click="uploadFile()">
                            <i class="el-icon-folder-add" />
                            Tải file lên (.jpeg, .png,.pdf)
                        </button>
                        <input ref="inputfile" type="file" class="opacity-0">
                    </div>
                </div>
                <div class="add" @click="addChiev()">
                    <i class="el-icon-circle-plus" />
                    <span class="text-[#E79000] text-[16px] ml-[18px]">Thêm thành tích</span>
                </div>
            </div>
            <div class="w-6/12 mt-10">
                <div v-for="item in listWorks" :key="item">
                    <img v-if="item !== listWorks[0]" src="@/static/img/vector.png" class="mt-[16px] mb-[16px]">
                    <div class="flex flex-col mt-[16px] mb-[16px]">
                        <span class="text-[16px] text-[#252733] ">Nghề nghiệp {{ item.id+1 }}</span>
                        <div ref="htmlWork">
                            <textarea placeholder="Nhập nội dung" class="mt-[8px] rounded-[4px] w-[456px] h-[176px] border border-[#FDF4E6] pb-[11px] pt-[11px] pr-[10px] pl-[16px]" />
                            <div ref="addWhere" />
                        </div>
                    </div>
                </div>
                <div class="add">
                    <i class="el-icon-circle-plus" />
                    <span class="text-[#E79000] text-[16px] ml-[18px]" @click="addWork()">Thêm nghề nghiệp</span>
                </div>
            </div>
        </div>
        <button class="mx-auto mb-[40px] bg-[#BF1014] rounded-[4px] text-[#fff] w-[382px] h-[48px] mt-[40px] text-[18px] font-bold leading-[48px]">
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
                listWorks: [
                    {
                        id: 0,
                        name: '',
                    },
                    {
                        id: 1,
                        name: '',
                    },
                ],
                fileList: [
                    {
                        name: '',
                        url: '',
                    },
                    {
                        name: '',
                        url: '',
                    },
                ],
                listAchievement: [
                    {
                        class: '',
                        academiclevel: '',
                    },
                    {
                        class: '',
                        academiclevel: '',
                    },
                ],
                iWork: 2,
                iAchie: 2,
            };
        },
        methods: {
            uploadFile() {
                this.$refs.inputfile.click();
            },
            addWork() {
                const work = {
                    id: this.iWork,
                    name: '',
                };
                this.listWorks.push(work);
                this.iWork += 1;
            },
            addChiev() {
                const chiev = {
                    class: '',
                    academiclevel: '',
                };
                this.listAchievement.push(chiev);
                this.iAchie += 1;
            },
        },
    };
</script>
<style scoped>
    .el-icon-circle-plus{
        font-size: 20px;
        color: #E79000;
    }
    *:focus {
        outline: none;
    }
    textarea {
        resize: none;
    }
    .add:hover{
        cursor: pointer;
    }
</style>
