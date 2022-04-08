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
        <div class="flex flex-row justify-items-start w-[856px] mx-auto">
            <div class="w-[152px] h-[152px] rounded-full mr-3">
                <img src="@/static/img/Avatar2021.png">
            </div>
            <div class="flex flex-col">
                <span class="text-[26px] font-bold text-[#1D1F2C]">
                    Lê Văn Thành
                    <span class="text-[18px] text-[#1D1F2C] font-normal">
                        (Lê Quốc Anh)
                    </span>
                </span>
                <div class="mt-2 text-[15px] text-[#75767E]">
                    Đời thứ 8 - Chi thứ 2
                </div>
            </div>
        </div>
        <div class="flex flex-row justify-items-start w-[856px] mx-auto mt-[45px]">
            <button class="w-[209px] h-[46px] text-[16px] text-[#474953]" :class="{ active: active1 }" @click="selectedTab('Ttcn')">
                Thông tin cá nhân
            </button>
            <button class="w-[209px] h-[46px] text-[16px] text-[#474953]" :class="{ active: active2 }" @click="selectedTab('Qhgd')">
                Quan hệ gia đình
            </button>
            <button class="w-[209px] h-[46px] text-[16px] text-[#474953]" :class="{ active: active3 }" @click="selectedTab('Hvnn')">
                Học vấn & Nghề nghiệp
            </button>
        </div>
        <div class="flex flex-row justify-items-start w-[856px] mx-auto">
            <keep-alive>
                <component :is="tab" />
            </keep-alive>
        </div>
    </div>
</template>
<script>
    import Ttcn from '@/components/thongtincanhan/Ttcn2.vue';
    import Qhgd from '@/components/thongtincanhan/Qhgd.vue';
    import Hvnn from '@/components/thongtincanhan/Hvnn.vue';

    export default {
        components: {
            Ttcn,
            Qhgd,
            Hvnn,
        },
        data() {
            return {
                tab: 'Ttcn',
                active1: true,
                active2: false,
                active3: false,
            };
        },
        methods: {
            selectedTab(tab) {
                this.tab = tab;
                if (tab === 'Ttcn') {
                    this.active1 = true;
                    this.active2 = false;
                    this.active3 = false;
                } else if (tab === 'Qhgd') {
                    this.active1 = false;
                    this.active2 = true;
                    this.active3 = false;
                } else if (tab === 'Hvnn') {
                    this.active1 = false;
                    this.active2 = false;
                    this.active3 = true;
                }
            },
        },
    };
</script>
<style scoped>
    .active{
        background-color: #BF1014;
        color: white;
        font-weight: bold;
        border-radius: 20px 20px 0 0;
    }
</style>
