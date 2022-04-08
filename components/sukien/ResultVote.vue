<template>
    <div class="bg-white p-6 mr-4 flex flex-col w-[680px] rounded-[4px] mb-6">
        <span class="text-[#252733] text-[16px] font-bold mb-6">Nội dung bình chọn</span>
        <div>
            <div
                v-for="item in items"
                :id="item.id"
                :key="item.id"
            >
                <div v-if="item.chose" class=" relative">
                    <div class="flex flex-row justify-between border border-[#F9E8CB] rounded-[4px] h-[45px]">
                        <div :style="{ width: (item.vote/totalVote)*100 + '%', opacity:  (item.vote/totalVote) }" class="bg-[#E79000] rounded-[4px]"></div>
                        <span class=" absolute left-0 leading-[45px] text-[16px] text-[#191B28] ml-3">{{ item.name }}</span>
                        <div class="w-[24px] h-[24px] border border-[#E79000] rounded-full relative mt-3 mr-3">
                            <div class="ball active" />
                        </div>
                    </div>
                    <div class="mt-1">
                        <span class="text-[#474953] text-[14px]">{{ item.vote }} phiếu ({{Math.round((item.vote/totalVote)*100)}}%)</span>
                    </div>
                </div>
                <div v-else class="relative">
                    <div class="flex flex-row justify-between border border-[#F9E8CB] rounded-[4px] h-[45px]">
                        <div :style="{ width: (item.vote/totalVote)*100 + '%', opacity:  (item.vote/totalVote) }" class="bg-[#E79000] w-3/12 rounded-[4px] opacity-40"></div>
                        <span class=" absolute left-0 leading-[45px] text-[16px] text-[#191B28] ml-3">{{ item.name }}</span>
                        <div class="w-[24px] h-[24px] border border-[#E79000] rounded-full relative mt-3 mr-3">
                            <div class="ball" />
                        </div>
                    </div>
                    <div class="mt-1">
                        <span class="text-[#474953] text-[14px]">{{ item.vote }} phiếu ({{Math.round((item.vote/totalVote)*100)}}%)</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>

    export default {
        components: {
        },
        props: [
            'items',
            'totalVote',
        ],
        data() {
            return {
            };
        },
    };
</script>
<style scoped>
    .ball {
        display: none;
    }
    .ball.active {
        display: block;
        width: 16px;
        height: 16px;
        background-color: #E79000;
        border-radius: 50px;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
    .el-icon-circle-plus{
        color: #E79000;
        font-size: 20px;
    }
    .check{
        width: 50%;
        top: 0;
        left: 0;
        opacity: .3;
    }
</style>
