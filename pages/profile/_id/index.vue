<template>
    <div class="mt-[140px] w-[768px] mx-auto">
        <div class="flex flex-row justify-items-start mb-[24px] w-[1032px] mx-auto ">
            <div class="inline-block">
                <span class="text-[16px] text-[#606266] mr-[13px]">Trang chủ</span>
                <i class="el-icon-arrow-right" />
                <span class="text-[16px] text-[#606266] mr-[13px]">Cá nhân</span>
                <i class="el-icon-arrow-right" />
                <span class="text-[16px] text-[#606266] font-bold">Thông tin cá nhân</span>
            </div>
        </div>
        <div>
            <img src="@/static/img/profile.png" class="mx-auto mt-[10px]">
        </div>
        <div class="flex flex-row justify-center mt-[45px]">
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
        <div class="flex flex-row justify-center">
            <keep-alive>
                <component :is="tab" />
            </keep-alive>
        </div>
    </div>
</template>
<script>
    import Ttcn from '@/components/profile/Ttcn.vue';
    import Qhgd from '@/components/profile/Qhgd.vue';
    import Hvnn from '@/components/profile/Hvnn.vue';

    export default {
        layout: 'profile',
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
