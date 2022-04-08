<template>
    <div class="w-[1032px] mx-auto mb-4">
        <div class="flex flex-row justify-items-start mb-[24px] w-[1032px] mx-auto">
            <div class="inline-block">
                <span class="text-[16px] text-[#606266] mr-[13px]">Trang chủ</span>
                <i class="el-icon-arrow-right mr-[13px]" />
                <span class="text-[16px] text-[#606266] mr-[13px]">Gia phả</span>
                <i class="el-icon-arrow-right mr-[13px]" />
                <span class="text-[16px] text-[#606266] font-bold">Tài liệu</span>
            </div>
        </div>
        <div class="w-[1032px] mx-auto text-[36px] font-bold flex flex-row justify-center">
            <span>Thông báo</span>
        </div>
        <div class="mt-6 flex flex-row justify-center text-[#474953] text-[16px]">
            <div class="cursor-pointer px-10 py-[10px] h-[46px]" :class="{active: active1}" @click="selectedTab('Events')">
                <span>Sự kiện (3)</span>
            </div>
            <div class="cursor-pointer px-10 py-[10px] h-[46px]" :class="{active: active2}" @click="selectedTab('News')">
                <span>Tin tức (2)</span>
            </div>
            <div class="cursor-pointer px-10 py-[10px] h-[46px]" :class="{active: active3}" @click="selectedTab('Requests')">
                <span>Yêu cầu (4)</span>
            </div>
            <div class="cursor-pointer px-10 py-[10px] h-[46px]" :class="{active: active4}" @click="selectedTab('Others')">
                <span>Khác (1)</span>
            </div>
        </div>
        <div class="mx-auto w-[856px]">
            <component :is="tab" />
        </div>
    </div>
</template>
<script>
    import Events from '@/components/thongbao/Events.vue';
    import News from '@/components/thongbao/News.vue';
    import Requests from '@/components/thongbao/Requests.vue';
    import Others from '@/components/thongbao/Others.vue';

    export default {
        components: {
            Events,
            News,
            Requests,
            Others,
        },
        data() {
            return {
                tab: 'Events',
                active1: true,
                active2: false,
                active3: false,
                active4: false,
            };
        },
        methods: {
            selectedTab(param) {
                this.tab = param;
                if (param === 'Events') {
                    this.active1 = true;
                    this.active2 = false;
                    this.active3 = false;
                    this.active4 = false;
                } else if (param === 'News') {
                    this.active1 = false;
                    this.active2 = true;
                    this.active3 = false;
                    this.active4 = false;
                } else if (param === 'Requests') {
                    this.active1 = false;
                    this.active2 = false;
                    this.active3 = true;
                    this.active4 = false;
                } else if (param === 'Others') {
                    this.active1 = false;
                    this.active2 = false;
                    this.active3 = false;
                    this.active4 = true;
                }
            },
        },
    };
</script>
<style scoped>
    .active {
        background-color: #BF1014;
        color: white;
        font-weight: bold;
        border-radius: 20px 20px 0px 0px;
    }
</style>
