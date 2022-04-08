<template>
    <div class=" w-[1032px] flex flex-col mx-auto">
        <div class="flex flex-row justify-items-start mb-[24px] w-[1032px] mx-auto">
            <div class="inline-block">
                <span class="text-[16px] text-[#606266] mr-[13px]">Trang chủ</span>
                <i class="el-icon-arrow-right" />
                <span class="text-[16px] text-[#606266] ">Sự kiện</span>
                <i class="el-icon-arrow-right" />
                <span class="text-[16px] text-[#606266] font-bold">Chi tiết sự kiện</span>
            </div>
        </div>
        <div>
            <img src="@/static/img/chitietsukien.png" class="mb-6">
        </div>
        <div>
            <span class="text-[#BF1014] text-[18px] font-bold">Thứ 2 - 12/12/2021 <span class="font-normal">(10/11/2021)</span> Lúc 8h30</span>
        </div>
        <div>
            <span class="text-[48px] text-[#252733] font-bold">Họp họ 2020</span>
        </div>
        <div class="flex flex-row justify-between">
            <div>
                <span class="text-[16px] text-[#252733]">Sự kiện họp họ hàng năm</span>
            </div>
            <div v-if="status === null" class="flex flex-row justify-between w-[328px]">
                <button class=" rounded-[4px] border text-[#BF1014] border-[#BF1014] font-bold text-[16px] w-[156px] h-[40px]" @click="noJoin()">
                    Từ chối
                </button>
                <button class=" rounded-[4px] border text-[#fff] bg-[#BF1014] font-bold text-[16px] w-[156px] h-[40px]" @click="join()">
                    Tham gia
                </button>
            </div>
            <div v-if="status" class="flex flex-row justify-between w-[328px]">
                <button @click="noJoin()" class=" rounded-[4px] border text-[#75767E] border-[#75767E] font-bold text-[16px] w-[156px] h-[40px]">
                    Hủy tham gia
                </button>
                <button class=" rounded-[4px] border text-[#fff] bg-[#E79000] font-bold text-[16px] w-[156px] h-[40px]">
                    <span> <i class="el-icon-success" /> Sẽ tham gia</span>
                </button>
            </div>
            <div v-if="status === false" class="flex flex-row justify-between w-[328px]">
                <button class=" rounded-[4px] border text-[#fff] bg-[#E79000] font-bold text-[16px] w-[156px] h-[40px]">
                    <span> <i class="el-icon-success" /> Đã từ chối</span>
                </button>
                <button @click="join()" class=" rounded-[4px] text-[#75767E] border border-[#75767E] font-bold text-[16px] w-[156px] h-[40px]">
                    Tham gia
                </button>
            </div>
        </div>
        <div class="flex flex-row justify-between mb-[30px] mt-6">
            <div class="w-[680px]">
                <div class="px-[24px] py-[24px] bg-white rounded-[4px]">
                    <div class="flex flex-row">
                        <div class="mr-[18px]">
                            <img src="@/static/img/clock.svg">
                        </div>
                        <div>
                            <div class="text-[#191B28] text-[16px] mb-2">
                                5 giờ 30 phút
                            </div>
                            <div class="text-[#30323E] text-[14px] mb-2">
                                08:30 - 12/12/2021 (10/11/2021)
                            </div>
                            <div class="text-[#30323E] text-[14px]">
                                14:00 - 12/12/2021 (10/11/2021)
                            </div>
                        </div>
                    </div>
                    <div class="flex flex-row mt-4">
                        <div class="mr-[18px]">
                            <img src="@/static/img/truongho.svg">
                        </div>
                        <div>
                            <div class="text-[#191B28] text-[16px]">
                                Trưởng họ, trưởng chi
                            </div>
                        </div>
                    </div>
                    <div class="flex flex-row mt-4">
                        <div class="mr-[18px]">
                            <img src="@/static/img/flag.svg">
                        </div>
                        <div>
                            <div class="text-[#191B28] text-[16px]">
                                Lê Đức Nam (Trưởng họ)
                            </div>
                        </div>
                    </div>
                    <div class="mt-6">
                        <span class="text-[#252733] text-[16px] font-bold">Nội dung sự kiện:</span>
                    </div>
                    <div class="mt-4">
                        <span class="text-[#252733] text-[16px]">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, ...</span>
                    </div>
                    <div class="mt-4">
                        <button class="text-[#369FFF] text-[14px]">
                            Xem thêm
                        </button>
                    </div>
                    <div class="mt-6">
                        <span class="font-bold text-[16px]">Trách nhiệm:</span>
                        <span>Bắt buộc</span>
                    </div>
                    <div class="flex flex-row justify-between mt-6">
                        <span class="font-bold text-[16px]">Album Ảnh</span>
                        <button class="text-[#369FFF] text-[14px]">
                            Xem thêm
                        </button>
                    </div>
                    <div class="flex flex-row justify-between mt-4">
                        <div class="w-[143px] h-[80px] rounded-[4px]">
                            <img src="@/static/img/img.png">
                        </div>
                        <div class="w-[143px] h-[80px] rounded-[4px]">
                            <img src="@/static/img/img.png">
                        </div>
                        <div class="w-[143px] h-[80px] rounded-[4px]">
                            <img src="@/static/img/img.png">
                        </div>
                        <div class="w-[143px] h-[80px] rounded-[4px]">
                            <img src="@/static/img/img.png">
                        </div>
                    </div>
                </div>
            </div>
            <div class="w-[328px]">
                <div class="px-[24px] py-[24px] bg-white rounded-[4px] h-[627px] overflow-y-scroll">
                    <Participants :title="title" />
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import Participants from '@/components/sukien/Participants.vue';

    export default {
        components: {
            Participants,
        },
        data() {
            return {
                title: 'Danh sách tham gia (50)',
                status: null,
            };
        },
        methods: {
            noJoin() {
                this.status = false;
            },
            join() {
                this.status = true;
            },

        },
    };
</script>
<style scoped>
    .el-icon-success{
        color: white;
        font-size: 20px;
    }
</style>
