<template>
    <div class="w-screen max-w-[1440px] flex flex-col mx-auto bg-[#FEF9F2]">
        <img src="@/static/img/bgtop.png">
        <div class="flex flex-col relative top-[-55px] z-[100]">
            <img src="@/static/img/reinfo.png" class="mx-auto ">
            <span class="text-center text-[16px] text-[#75767E] mt-[29px] mb-[50px]">Vui lòng điền đầy đủ thông tin cá nhân để có thể sử dụng các tính năng của App</span>
            <div class="flex flex-row justify-center">
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
        <img src="@/static/img/bgbottom.png">
    </div>
</template>
<script>
    import Ttcn from '@/components/info/Ttcn.vue';
    import Qhgd from '@/components/info/Qhgd.vue';
    import Hvnn from '@/components/info/Hvnn.vue';

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
        layout: 'auth',
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
