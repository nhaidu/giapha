<template>
    <div class=" relative bg-[#FEF9F2] flex flex-col ">
        <!-- <img src="../../static/img/bgtop.png" class="w-full h-[143px]"> -->
        <div class="flex flex-row justify-items-start mb-[24px] w-[1032px] mx-auto">
            <div class="inline-block">
                <span class="text-[16px] text-[#606266] mr-[13px]">Trang chủ</span>
                <i class="el-icon-arrow-right" />
                <span class="text-[16px] text-[#606266] font-bold">Sự kiện</span>
            </div>
        </div>
        <div class="flex flex-row justify-center mb-[34px]">
            <div class="mr-[24px]">
                <button class="w-[416px] h-[48px] bg-[#E79000] text-[#fff] text-[18px] font-bold rounded-[4px]">
                    Thêm sự kiện
                </button>
                <div class=" mt-6">
                    <SmallCalendar />
                </div>
                <div class="mt-[24px] flex flex-row justify-between">
                    <span class="font-bold text-[18px] text-[#252733]">Sự kiện sắp tới</span>
                    <span class="text-[#369FFF] text-[14px]">Xem tất cả</span>
                </div>
                <div class="mt-[24px]">
                    <el-timeline>
                        <el-timeline-item :color="'#E79000'" placement="top">
                            <div class=" w-[416px] h-[114px] mx-auto mt-[16px] flex flex-row justify-between px-4">
                                <div class="flex flex-row">
                                    <div class="flex flex-row">
                                        <img src="@/static/img/bird.png" class="mr-[11px] h-[20px]">
                                    </div>
                                    <div class="h-[26px]">
                                        <div>
                                            <span class="text-[16px] leading-[24px] text-[#252733] mr-4">11:00</span> <span class="text-[16px] text-[#252733] mr-4">20/11/2021</span>
                                        </div>
                                        <div class="mt-[4px]">
                                            <span class="text-[16px] leading-6 font-bold text-[#252733]">Sinh nhật Lê Mai</span>
                                        </div>
                                        <div class="mt-[4px] text-[14px] leading-6 text-[#75767E]">
                                            Lorem Ipsum is simply dummy text of ...
                                        </div>
                                    </div>
                                </div>
                                <div class="w-[80px] h-[80px] rounded-full gato" />
                            </div>
                        </el-timeline-item>
                        <el-timeline-item :color="'#E79000'" placement="top">
                            <div class=" w-[416px] h-[114px] mx-auto mt-[16px] flex flex-row justify-between px-4">
                                <div class="flex flex-row">
                                    <div class="flex flex-row">
                                        <img src="@/static/img/gio.png" class="mr-[11px] h-[20px]">
                                    </div>
                                    <div class="h-[26px]">
                                        <div>
                                            <span class="text-[16px] leading-[24px] text-[#252733] mr-4">11:00</span> <span class="text-[16px] text-[#252733] mr-4">5/12/2021</span>
                                        </div>
                                        <div class="mt-[4px]">
                                            <span class="text-[16px] leading-6 font-bold text-[#252733]">Giỗ ông Lê Văn Lương</span>
                                        </div>
                                        <div class="mt-[4px] text-[14px] leading-6 text-[#75767E]">
                                            Lorem Ipsum is simply dummy text of ...
                                        </div>
                                    </div>
                                </div>
                                <div class="w-[80px] h-[80px] rounded-full gato2" />
                            </div>
                        </el-timeline-item>
                        <el-timeline-item :color="'#E79000'" placement="top">
                            <div class=" w-[416px] h-[114px] mx-auto mt-[16px] flex flex-row justify-between px-4">
                                <div class="flex flex-row">
                                    <div class="flex flex-row relative">
                                        <img src="@/static/img/people.png" class="mr-[11px] h-[20px]">
                                    </div>
                                    <div class="h-[26px]">
                                        <div>
                                            <span class="text-[16px] leading-[24px] text-[#252733] mr-4">11:00</span> <span class="text-[16px] text-[#252733] mr-4">20/12/2021</span>
                                        </div>
                                        <div class="mt-[4px]">
                                            <span class="text-[16px] leading-6 font-bold text-[#252733]">Họp họ</span>
                                        </div>
                                        <div class="mt-[4px] text-[14px] leading-6 text-[#75767E]">
                                            Lorem Ipsum is simply dummy text of ...
                                        </div>
                                    </div>
                                </div>
                                <div class="w-[80px] h-[80px] rounded-full gato3" />
                            </div>
                        </el-timeline-item>
                    </el-timeline>
                </div>
            </div>
            <div class="bg-[#fff] w-[592px] min-h-[836px] py-[24px] px-[24px] flex flex-col rounded-[4px]">
                <span class="text-[18px] text-[#252733] font-bold">Hôm nay</span>
                <div class="bg-[#BF1014] w-[544px] h-[126px] mx-auto mt-[16px] rounded-[4px] flex flex-row justify-evenly">
                    <div class="flex flex-col justify-center py-4">
                        <span class=" font-bold text-[16px] text-[#fff] mx-auto my-auto">Giờ</span>
                        <span class=" font-bold text-[24px] text-[#fff] mx-auto my-auto">13:20</span>
                        <span class=" font-bold text-[14px] text-[#fff] mx-auto my-auto">Quí Mùi</span>
                    </div>
                    <div class="flex flex-col justify-center py-4">
                        <span class=" font-bold text-[16px] text-[#fff] mx-auto my-auto">Ngày</span>
                        <span class=" font-bold text-[24px] text-[#fff] mx-auto my-auto">23 <span class="text-[#E59FA1]">(24)</span> </span>
                        <span class=" font-bold text-[14px] text-[#fff] mx-auto my-auto">Canh Tuất</span>
                    </div>
                    <div class="flex flex-col justify-center py-4">
                        <span class=" font-bold text-[16px] text-[#fff] mx-auto my-auto">Tháng</span>
                        <span class=" font-bold text-[24px] text-[#fff] mx-auto my-auto">10 <span class="text-[#E59FA1]">(9)</span> </span>
                        <span class=" font-bold text-[14px] text-[#fff] mx-auto my-auto">Mật Tuất</span>
                    </div>
                    <div class="flex flex-col justify-center py-4">
                        <span class=" font-bold text-[16px] text-[#fff] mx-auto my-auto">Năm</span>
                        <span class=" font-bold text-[24px] text-[#fff] mx-auto my-auto">2021 </span>
                        <span class=" font-bold text-[14px] text-[#fff] mx-auto my-auto">Tân Sửu</span>
                    </div>
                </div>
                <div class="bg-[#fff] w-[544px] h-[114px] mx-auto mt-[16px] rounded-[4px] card flex flex-row justify-between py-4 px-4">
                    <div class="flex flex-row">
                        <div>
                            <img src="@/static/img/bird.png" class="mr-[11px] h-[20px]">
                        </div>
                        <div class="h-[26px]">
                            <div>
                                <span class="text-[16px] leading-[24px] text-[#252733] mr-4">11:00</span> <span class="text-[16px] text-[#252733] mr-4">Hôm nay</span>
                            </div>
                            <div class="mt-[4px]">
                                <span class="text-[16px] leading-6 font-bold text-[#252733]">Sinh nhật Lê Mai</span>
                            </div>
                            <div class="mt-[4px] text-[14px] leading-6 text-[#75767E]">
                                Lorem Ipsum is simply dummy text of the printing and ...
                            </div>
                        </div>
                    </div>
                    <div class="w-[80px] h-[80px] rounded-full gato" />
                </div>
                <div class="bg-[#fff] w-[544px] h-[114px] mx-auto mt-[16px] rounded-[4px] card flex flex-row justify-between py-4 px-4">
                    <div class="flex flex-row">
                        <div>
                            <img src="@/static/img/bird.png" class="mr-[11px] h-[20px]">
                        </div>
                        <div class="h-[26px]">
                            <div>
                                <span class="text-[16px] leading-[24px] text-[#252733] mr-4">11:00</span> <span class="text-[16px] text-[#252733] mr-4">Hôm nay</span>
                            </div>
                            <div class="mt-[4px]">
                                <span class="text-[16px] leading-6 font-bold text-[#252733]">Sinh nhật Lê Mai</span>
                            </div>
                            <div class="mt-[4px] text-[14px] leading-6 text-[#75767E]">
                                Lorem Ipsum is simply dummy text of the printing and ...
                            </div>
                        </div>
                    </div>
                    <div class="w-[80px] h-[80px] rounded-full gato" />
                </div>
                <div class="bg-[#fff] w-[544px] h-[114px] mx-auto mt-[16px] rounded-[4px] card flex flex-row justify-between py-4 px-4">
                    <div class="flex flex-row">
                        <div>
                            <img src="@/static/img/bird.png" class="mr-[11px] h-[20px]">
                        </div>
                        <div class="h-[26px]">
                            <div>
                                <span class="text-[16px] leading-[24px] text-[#252733] mr-4">11:00</span> <span class="text-[16px] text-[#252733] mr-4">Hôm nay</span>
                            </div>
                            <div class="mt-[4px]">
                                <span class="text-[16px] leading-6 font-bold text-[#252733]">Sinh nhật Lê Mai</span>
                            </div>
                            <div class="mt-[4px] text-[14px] leading-6 text-[#75767E]">
                                Lorem Ipsum is simply dummy text of the printing and ...
                            </div>
                        </div>
                    </div>
                    <div class="w-[80px] h-[80px] rounded-full gato" />
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import SmallCalendar from '@/components/sukien/SmallCalendar.vue';

    export default {
        layout: 'default',
        components: {
            SmallCalendar,
        },
    };
</script>
<style scoped>
    .el-icon-arrow-right{
        font-size: 14px;
        color: #C0C4CC;
        margin-right: 13px;
    }
    .card{
        box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.05);
        margin-bottom: 16px;
    }
    .gato{
        background-image: url('@/static/img/gato.png');
        background-position: center;
        background-repeat: no-repeat;
    }
    .gato2{
        background-image: url('@/static/img/gioo.png');
        background-position: center;
        background-repeat: no-repeat;
    }
    .gato3{
        background-image: url('@/static/img/hop.png');
        background-position: center;
        background-repeat: no-repeat;
    }
    .dot{
        height: 100%;
        width: 2px;
        background-color: #E79000;
    }
</style>
