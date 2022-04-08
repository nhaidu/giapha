<template>
    <div class="flex flex-col w-[240px]">
        <span class="text-[16px] text-[#252733] font-bold"> {{ title }} </span>
        <div class="mt-6 flex flex-col">
            <div v-for="item in checkBoxData" :key="item.id">
                <div v-if="item.chose && item.id<5" class="cursor-pointer mb-[18px] flex flex-row" @click="checkedBox(item.id)">
                    <div class="w-[24px] h-[24px] rounded-full border border-[#A3A4A9] relative">
                        <i class="el-icon-success" />
                    </div>
                    <div>
                        <span class="ml-4 leading-[24px] text-[16px] "> {{ item.name }} </span>
                    </div>
                </div>
                <div v-if="!item.chose && item.id<5" class="cursor-pointer mb-[18px] flex flex-row" @click="checkedBox(item.id)">
                    <div class="w-[24px] h-[24px] rounded-full border border-[#A3A4A9] bg-white relative" />
                    <div>
                        <span class="ml-4 leading-[24px] text-[16px]">{{ item.name }}</span>
                    </div>
                </div>
            </div>
        </div>
        <div v-if="checkBoxData.length>=5 && !readMore" class=" cursor-pointer mb-[18px] text-[#369FFF] text-[16px]" @click="readMore=true">
            Xem thêm
        </div>
        <div v-if="readMore">
            <div class=" flex flex-col">
                <div v-for="item in checkBoxData" :key="item.id">
                    <div v-if="item.chose && item.id>=5" class="cursor-pointer mb-[18px] flex flex-row" @click="checkedBox(item.id)">
                        <div class="w-[24px] h-[24px] rounded-full border border-[#A3A4A9] relative">
                            <i class="el-icon-success" />
                        </div>
                        <div>
                            <span class="ml-4 leading-[24px] text-[16px] "> {{ item.name }} </span>
                        </div>
                    </div>
                    <div v-if="!item.chose && item.id>=5" class="cursor-pointer mb-[18px] flex flex-row" @click="checkedBox(item.id)">
                        <div class="w-[24px] h-[24px] rounded-full border border-[#A3A4A9] bg-white relative" />
                        <div>
                            <span class="ml-4 leading-[24px] text-[16px]">{{ item.name }}</span>
                        </div>
                    </div>
                </div>
            </div>
            <div class=" cursor-pointer mb-[18px] text-[#369FFF] text-[16px]" @click="readMore=false">
                Thu gọn
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        props: {
            checkBoxData: {
                type: Array,
                required: true,
            },
            title: {
                type: String,
                required: true,
            },
        },
        data() {
            return {
                readMore: false,
            };
        },
        methods: {
            checkedBox(param) {
                this.$emit('checkedBox', param);
            },
        },
    };
</script>
<style>
    .el-icon-success{
        color: #BF1014;
        font-size: 24px;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
</style>
