<template>
    <div class="w-[1032px] mx-auto flex flex-col">
        <div class="w-[1032px] mx-auto flex flex-col">
            <div class="flex flex-row justify-items-start mb-[24px] w-[1032px] mx-auto">
                <div class="inline-block">
                    <span class="text-[16px] text-[#606266] mr-[13px]">Trang chủ</span>
                    <i class="el-icon-arrow-right" />
                    <span class="text-[16px] text-[#606266] mr-[13px]">Thống kê</span>
                    <i class="el-icon-arrow-right" />
                    <span class="text-[16px] text-[#606266] font-bold">Thu chi</span>
                </div>
            </div>
            <div class="w-[1032px] mt-6 tetx-[#252733] text-[36px] font-bold flex flex-row">
                <div class="mr-6">
                    Quỹ khuyến học
                </div>
                <i class="el-icon-info" />
            </div>
            <div class="flex flex-row w-[1032px] mt-5">
                <div class="w-[592px] flex flex-col mr-6">
                    <div>
                        <el-input
                            placeholder="Nhập tên để tìm kiếm"
                            suffix-icon="el-icon-search"
                        />
                    </div>
                    <div class="mt-8 flex flex-row text-[16px]">
                        <div class="mr-10 cursor-pointer" :class="{ active: active1 }" @click="selectedTab('DaThu')">
                            Đã thu (1.200)
                        </div>
                        <div class=" cursor-pointer" :class="{ active: active2 }" @click="selectedTab('ChuaThu')">
                            Chưa thu (3)
                        </div>
                    </div>
                    <div class="mt-2">
                        <keep-alive>
                            <component :is="tab" />
                        </keep-alive>
                    </div>
                </div>
                <div class="w-[415px] flex flex-col">
                    <div class="date">
                        <el-date-picker
                            type="date"
                            placeholder="Chọn khoảng thời gian"
                        />
                    </div>
                    <div class="mt-8 text-[16px] text-[#BF1014] font-bold">
                        Đã chi (2)
                    </div>
                    <div class="mt-2">
                        <DaChi />
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import DaThu from '@/components/baocao/DaThu.vue';
    import ChuaThu from '@/components/baocao/ChuaThu.vue';
    import DaChi from '@/components/baocao/DaChi.vue';

    export default {
        components: {
            DaThu,
            ChuaThu,
            DaChi,
        },
        data() {
            return {
                tab: 'DaThu',
                active1: true,
                active2: false,
            };
        },
        methods: {
            selectedTab(tab) {
                this.tab = tab;
                if (tab === 'DaThu') {
                    this.active1 = true;
                    this.active2 = false;
                } else if (tab === 'ChuaThu') {
                    this.active1 = false;
                    this.active2 = true;
                }
            },
        },
    };
</script>
<style scoped>
    .el-icon-info{
        margin: auto 0;
    }
    .active {
        color: #BF1014;
        font-weight: bold;
    }
</style>
<style>
    input.el-input__inner {
        height: 48px;
    }
    .date input.el-input__inner {
        width: 416px;
    }
</style>
