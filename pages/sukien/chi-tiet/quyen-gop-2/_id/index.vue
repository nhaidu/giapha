<template>
    <div class="w-[1032px] mx-auto flex flex-col">
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
            <span class="text-[48px] text-[#252733] font-bold">Quỹ khuyến học 2021</span>
        </div>
        <div class="flex flex-row justify-between">
            <div class="w-[599px]">
                <span class="text-[16px] text-[#252733]">Nhằm mục đích tạo điều kiện cho con, em, cháu trong dòng họ có được điều kiện học tập tốt nhất!</span>
            </div>
            <div v-if="!isUpload" class="flex flex-row justify-between relative" >
                <input type="file" class=" absolute top-0 left-0 w-[328px] h-[40px] opacity-0" @click="upload()">
                <button class=" rounded-[4px] border text-[#fff] bg-[#BF1014] font-bold text-[16px] w-[328px] h-[40px]">
                    Tải file lên
                </button>
            </div>
            <div v-else class="flex flex-row justify-between relative">
                <button class=" rounded-[4px] text-[#E79000] border border-[#E79000] font-bold text-[16px] w-[328px] h-[40px]">
                    Xem file đã tải
                </button>
            </div>
        </div>
        <div class="bg-[#fff] p-[26px] mt-6">
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
                        Tất cả
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
            <div class="flex flex-row mt-4">
                <div class="w-[143px] h-[80px] rounded-[4px] mr-4">
                    <img src="@/static/img/img.png">
                </div>
                <div class="w-[143px] h-[80px] rounded-[4px] mr-4">
                    <img src="@/static/img/img.png">
                </div>
                <div class="w-[143px] h-[80px] rounded-[4px] mr-4">
                    <img src="@/static/img/img.png">
                </div>
                <div class="w-[143px] h-[80px] rounded-[4px] mr-4">
                    <img src="@/static/img/img.png">
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                isUpload: false,
            };
        },
        methods: {
            upload() {
                this.isUpload = true;
            },
        },

    };
</script>
<style scoped>

</style>
