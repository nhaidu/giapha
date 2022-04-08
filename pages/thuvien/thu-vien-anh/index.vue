<template>
    <div class="mt-[10px] bg-[#FEF9F2] pb-10">
        <div class="w-[1032px] mx-auto">
            <div class="w-[1032px] flex flex-row justify-items-start mb-[24px]">
                <div class="inline-block">
                    <span class="text-[16px] text-[#606266] mr-[13px]">Trang chủ</span>
                    <i class="el-icon-arrow-right mr-[13px]" />
                    <span class="text-[16px] text-[#606266] mr-[13px]">Thống kê</span>
                    <i class="el-icon-arrow-right mr-[13px]" />
                    <span class="text-[16px] text-[#606266] font-bold">Thư viện ảnh</span>
                </div>
            </div>
            <div class="flex flex-row justify-between" />
            <div class="flex flex-row">
                <div class="w-[260px] flex flex-col">
                    <span class="text-[36px] font-bold text-[#252733]">Thư viện ảnh</span>
                    <div class="flex flex-row mb-6 mt-6 cursor-pointer" @click="selectedTab('All')">
                        <div class="my-auto">
                            <img ref="allicon" src="@/static/img/photoicon.svg" class="my-auto mr-3 hidden">
                        </div>
                        <div class="my-auto">
                            <img ref="allred" src="@/static/img/allred.svg" class="my-auto mr-3 ">
                        </div>
                        <div class="text-[16px] text-[#75767E] font-bold">
                            <span ref="all" class="active">Chung</span>
                        </div>
                    </div>
                    <div class="flex flex-row mb-6 cursor-pointer" @click="selectedTab('Events')">
                        <div class="my-auto">
                            <img ref="eventicon" src="@/static/img/news.svg" class="my-auto mr-3">
                        </div>
                        <div class="my-auto">
                            <img ref="eventred" src="@/static/img/eventred.svg" class="my-auto mr-3 hidden">
                        </div>
                        <div class="text-[16px] text-[#75767E] font-bold">
                            <span ref="event">Sự kiện</span>
                        </div>
                    </div>
                    <div class="flex flex-row mb-6 cursor-pointer" @click="selectedTab('News')">
                        <div class="my-auto">
                            <img ref="newsicon" src="@/static/img/tintucicon.svg" class="my-auto mr-3 ">
                        </div>
                        <div class="my-auto">
                            <img ref="newsred" src="@/static/img/newsred.svg" class="my-auto mr-3 hidden">
                        </div>
                        <div class="text-[16px] text-[#75767E] font-bold">
                            <span ref="new">Tin tức</span>
                        </div>
                    </div>
                    <div class="flex flex-row mb-6 cursor-pointer" @click="selectedTab('Avatar')">
                        <div ref="avataricon" class="my-auto">
                            <img src="@/static/img/avataricon.svg" class="my-auto mr-3">
                        </div>
                        <div ref="avatarred" class="my-auto hidden">
                            <img src="@/static/img/avatarred.svg" class="my-auto mr-3">
                        </div>
                        <div class="text-[16px] text-[#75767E] font-bold">
                            <span ref="avatar">Ảnh đại diện</span>
                        </div>
                    </div>
                </div>
                <div class="flex flex-col w-[770px]">
                    <component :is="tab" />
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import All from '@/components/thuvienanh/All.vue';
    import Events from '@/components/thuvienanh/Events.vue';
    import News from '@/components/thuvienanh/News.vue';
    import Avatar from '@/components/thuvienanh/Avatar.vue';

    export default {
        layout: 'default',
        components: {
            All,
            Events,
            News,
            Avatar,
        },
        data() {
            return {
                tab: 'All',
            };
        },
        methods: {
            selectedTab(param) {
                if (this.tab === 'Avatar') {
                    this.$refs.avataricon.classList.remove('hidden');
                    this.$refs.avatarred.classList.add('hidden');
                    this.$refs.avatar.classList.remove('active');
                }
                if (this.tab === 'All') {
                    this.$refs.allicon.classList.remove('hidden');
                    this.$refs.allred.classList.add('hidden');
                    this.$refs.all.classList.remove('active');
                }
                if (this.tab === 'Events') {
                    this.$refs.eventicon.classList.remove('hidden');
                    this.$refs.eventred.classList.add('hidden');
                    this.$refs.event.classList.remove('active');
                }
                if (this.tab === 'News') {
                    this.$refs.newsicon.classList.remove('hidden');
                    this.$refs.newsred.classList.add('hidden');
                    this.$refs.new.classList.remove('active');
                }
                this.tab = param;
                if (param === 'Avatar') {
                    this.$refs.avataricon.classList.add('hidden');
                    this.$refs.avatarred.classList.remove('hidden');
                    this.$refs.avatar.classList.add('active');
                }
                if (param === 'All') {
                    this.$refs.allicon.classList.add('hidden');
                    this.$refs.allred.classList.remove('hidden');
                    this.$refs.all.classList.add('active');
                }
                if (param === 'News') {
                    this.$refs.newsicon.classList.add('hidden');
                    this.$refs.newsred.classList.remove('hidden');
                    this.$refs.new.classList.add('active');
                }
                if (param === 'Events') {
                    this.$refs.eventicon.classList.add('hidden');
                    this.$refs.eventred.classList.remove('hidden');
                    this.$refs.event.classList.add('active');
                }
            },
        },
    };
</script>
<style scoped>
    .active{
        color: #BF1014;
    }
</style>
