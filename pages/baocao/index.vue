<template>
    <div class="w-[1032px] mx-auto">
        <div class="flex flex-row justify-items-start mb-[24px] w-[1032px] mx-auto">
            <div class="inline-block">
                <span class="text-[16px] text-[#606266] mr-[13px]">Trang chủ</span>
                <i class="el-icon-arrow-right mr-[13px]" />
                <span class="text-[16px] text-[#606266] font-bold">Thống kê</span>
            </div>
        </div>
        <div class="w-[1032px] h-[308px] bg-white p-10 flex flex-row justify-between">
            <div class="flex flex-col w-[427px]">
                <div class="flex flex-row justify-between">
                    <img src="@/static/img/thuchi.png">
                    <span class="text-[#369FFF] text-[14px] cursor-pointer" @click="xemChiTiet('thuchi')">Xem chi tiết</span>
                </div>
                <div class="mt-4">
                    <span class="text-[14px] text-[#252733]">
                        Tổng thu:
                        <span class="text-[16px] font-bold">100.000.000 đ</span>
                    </span>
                </div>
                <div class="flex flex-row mt-5">
                    <div class="w-[120px]">
                        <Pie :datachart="datachart" :options="options" />
                    </div>
                    <div class="ml-6">
                        <div class="flex -flex-row">
                            <div class="w-8 h-4 bg-[#BF1014] my-auto mr-4" />
                            <div>
                                <span class="text-[16px] text-[#252733]">
                                    Chi:
                                    <span class="text-[20px] font-bold">80.000.000đ</span>
                                </span>
                            </div>
                        </div>
                        <div class="flex -flex-row">
                            <div class="w-8 h-4 bg-[#E79000] my-auto mr-4" />
                            <div>
                                <span class="text-[14px] text-[#252733]">
                                    Còn lại:
                                    <span class="text-[20px] font-bold">20.000.000đ</span>
                                </span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="flex flex-col w-[427px]">
                <div class="flex flex-row justify-between">
                    <img src="@/static/img/nhanso.png">
                    <span class="text-[#369FFF] text-[14px] cursor-pointer" @click="xemChiTiet('nhanso')">Xem chi tiết</span>
                </div>
                <div class="mt-4">
                    <span class="text-[14px] text-[#252733]">
                        Tổng cộng:
                        <span class="text-[20px] font-bold">1.700.000 người</span>
                    </span>
                </div>
                <div class="flex flex-row mt-5">
                    <div class="w-[120px]">
                        <Pie :datachart="datachart" :options="options" />
                    </div>
                    <div class="ml-6">
                        <div class="flex -flex-row">
                            <div class="w-8 h-4 bg-[#BF1014] my-auto mr-4 mb-[14px]" />
                            <div>
                                <span class="text-[14px] text-[#252733]">
                                    Còn sống:
                                    <span class="">1.200.000 người</span>
                                </span>
                            </div>
                        </div>
                        <div class="flex -flex-row">
                            <div class="w-8 h-4 bg-[#E79000] my-auto mr-4" />
                            <div>
                                <span class="text-[14px] text-[#252733]">
                                    Đã mất:
                                    <span class="text-[14px] ">500.000 người</span>
                                </span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="w-[1032px] flex flex-row justify-between mt-6  ">
            <div class="bg-white w-[504px] h-[765px] overflow-y-scroll py-10 px-10">
                <Quy />
            </div>
            <div class="flex flex-col w-[504px]">
                <div class="h-[396px] bg-white p-10">
                    <span class="text-[#191B28] text-[18px] font-bold ">Giới tính</span>
                    <div class="flex flex-row mt-2">
                        <div class="w-[106px]">
                            <Doughnut :data-doughnut="dataDoughnut" :options-doughnut="optionsDoughnut" />
                        </div>
                        <div class="ml-6">
                            <div class="flex -flex-row">
                                <div class="w-8 h-4 bg-[#D97072] my-auto mr-4 mb-[14px]" />
                                <div>
                                    <span class="text-[14px] text-[#252733]">
                                        Nam
                                        <span class="">(1.200.000 người)</span>
                                    </span>
                                </div>
                            </div>
                            <div class="flex -flex-row">
                                <div class="w-8 h-4 bg-[#E59FA1] my-auto mr-4 mb-[14px]" />
                                <div>
                                    <span class="text-[14px] text-[#252733]">
                                        Nữ
                                        <span class="text-[14px]">(500.000 người)</span>
                                    </span>
                                </div>
                            </div>
                            <div class="flex -flex-row">
                                <div class="w-8 h-4 bg-[#F2CFD0] my-auto mr-4" />
                                <div>
                                    <span class="text-[14px] text-[#252733]">
                                        Khác
                                        <span class="text-[14px]">(500.000 người)</span>
                                    </span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="mt-10">
                        <span class="text-[#191B28] text-[18px] font-bold ">Dâu / Rể</span>
                    </div>
                    <div class="flex flex-row mt-2">
                        <div class="w-[106px]">
                            <Doughnut :data-doughnut="dataDoughnut2" :options-doughnut="optionsDoughnut2" />
                        </div>
                        <div class="ml-6">
                            <div class="flex -flex-row mb-[14px]">
                                <div class="w-8 h-4 bg-[#E79000] my-auto mr-4" />
                                <div>
                                    <span class="text-[14px] text-[#252733]">
                                        Con Dâu
                                        <span class="">(70 người)</span>
                                    </span>
                                </div>
                            </div>
                            <div class="flex -flex-row">
                                <div class="w-8 h-4 bg-[#F5D399] my-auto mr-4" />
                                <div>
                                    <span class="text-[14px] text-[#252733]">
                                        Con Rể
                                        <span class="text-[14px]">(50 người)</span>
                                    </span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="flex flex-row p-10 h-[345px] mt-6 bg-white">
                    <div class="flex flex-col w-12">
                        <div v-for="item in bar" :key="item.id" class="relative group ">
                            <div :style="{ height: (item.value/total)*100*2.65 + 'px', backgroundColor: item.bg }" class="w-full mb-[1px]" />
                            <div class="group-hover:block w-[111px] bg-[#191B28] opacity-70 rounded-[4px] absolute left-[54px] top-0 hidden p-2">
                                <span class=" text-[12px] text-white"> {{ item.title }} tuổi <span class="text-[14px] font-bold"> {{ Math.round((item.value/total)*100) }} % </span></span>
                            </div>
                        </div>
                    </div>
                    <div class="flex flex-col ml-20 my-auto">
                        <div v-for="item in bar" :key="item.id">
                            <div class="flex flex-row">
                                <div :style="{backgroundColor: item.bg}" class="my-auto mb-[14px] w-6 h-4" />
                                <div class="ml-2">
                                    <span class="text-[14px]"> {{ item.title }} tuổi</span>
                                    <span>({{ item.value }} .000 nguời)</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="w-[1032px] bg-white mt-6 mb-12 p-10 flex flex-col">
            <span class="text-[16px]">Phát triển dòng họ</span>
            <div class="flex flex-col mt-4 mb-4">
                <div class="flex flex-row mb-2">
                    <div class="mr-2 flex flex-row">
                        <div class="w-[6px] h-[6px] border border-[#CB3D41] rounded-full my-auto" />
                        <div class="w-4 border border-[#CB3D41] h-[1px] bg-[#CB3D41] my-auto" />
                    </div>
                    <div class="text-[12px]">
                        Số thành viên được sinh ra
                    </div>
                </div>
                <div class="flex flex-row mb-2">
                    <div class="mr-2 flex flex-row">
                        <div class="w-[6px] h-[6px] border border-[#E79000] rounded-full my-auto" />
                        <div class="w-4 border border-[#E79000] h-[1px] bg-[#E79000] my-auto" />
                    </div>
                    <div class="text-[12px]">
                        Số thành viên đã mất
                    </div>
                </div>
            </div>
            <div class="mt-4 h-[401px]">
                <line-chart :chartdata="dataline" :options="optionsline" />
            </div>
        </div>
    </div>
</template>
<script>
    import Line from '@/components/chart/line.vue';
    import Pie from '@/components/chart/pie.vue';
    import Doughnut from '@/components/chart/doughnut.vue';
    import Quy from '@/components/baocao/quy.vue';

    export default {
        components: {
            Pie,
            Quy,
            Doughnut,
            lineChart: Line,
        },
        data() {
            return {
                total: 8000,
                bar: [
                    {
                        id: 0,
                        title: '0-5',
                        value: 500,
                        bg: '#E79000',
                    },
                    {
                        id: 1,
                        title: '6-17',
                        value: 500,
                        bg: '#ECA633',
                    },
                    {
                        id: 2,
                        title: '18-39',
                        value: 500,
                        bg: '#F1BC66',
                    },
                    {
                        id: 3,
                        title: '40-59',
                        value: 500,
                        bg: '#F5D399',
                    },
                    {
                        id: 4,
                        title: '60-69',
                        value: 1200,
                        bg: '#F2CFD0',
                    },
                    {
                        id: 5,
                        title: '70-79',
                        value: 1200,
                        bg: '#E59FA1',
                    },
                    {
                        id: 6,
                        title: '80-89',
                        value: 1200,
                        bg: '#D97072',
                    },
                    {
                        id: 7,
                        title: '90-99',
                        value: 1200,
                        bg: '#CC4043',
                    },
                    {
                        id: 8,
                        title: '>=100',
                        value: 1200,
                        bg: '#BF1014',
                    },
                ],
                dataline: {
                    labels: ['1945', '1950', '1955', '1960', '1965', '1970', '1975', '1980', '1985', '1990', '1995', '2010', '2015', '2020'],
                    datasets: [{
                                   data: [60, 80, 30, 42, 65, 75, 79, 18, 65, 38, 0, 55, 40, 30],
                                   fill: false,
                                   borderColor: '#CB3D41',
                                   tension: 0,
                                   borderWidth: 1.5,
                                   radius: 5,
                                   backgroundColor: '#fff',
                               },
                               {
                                   data: [25, 21, 3, 3, 20, 18, 57, 15, 60, 57, 25, 5, 65, 40],
                                   fill: false,
                                   borderColor: '#E79000',
                                   tension: 0,
                                   borderWidth: 1.5,
                                   radius: 5,
                                   backgroundColor: '#fff',
                               }],
                },
                optionsline: {
                    responsive: true,
                    maintainAspectRatio: false,
                    legend: {
                        display: false,
                    },
                    elements: {

                    },
                },
                dataDoughnut2: {
                    labels: [
                        'Con Dâu',
                        'Con Rể',
                    ],
                    datasets: [{
                        data: [70, 50],
                        backgroundColor: [
                            '#F5D399',
                            '#E79000',
                        ],
                    }],
                },
                optionsDoughnut2: {
                    legend: {
                        display: false,
                    },
                },
                dataDoughnut: {
                    labels: [
                        'Nam',
                        'Nữ',
                        'Khác',
                    ],
                    datasets: [{
                        data: [120, 50, 50],
                        backgroundColor: [
                            '#D97072',
                            '#E59FA1',
                            '#F2CFD0',
                        ],
                    }],
                },
                optionsDoughnut: {
                    legend: {
                        display: false,
                    },
                },
                datachart: {
                    labels: [
                        'Chi: 80.000.000 đ',
                        'Còn lại: 20.000.000 đ ',
                    ],
                    datasets: [{
                        data: [80, 20],
                        backgroundColor: [
                            '#BF1014',
                            '#E79000',
                        ],
                    }],
                },
                options: {
                    legend: {
                        display: false,
                    },
                },
            };
        },
        methods: {
            xemChiTiet(param) {
                if (param === 'thuchi') {
                    this.$router.push('/baocao/thuchi');
                } else if (param === 'nhanso') {
                    this.$router.push('/baocao/nhanso');
                }
            },
        },
    };
</script>

<style scoped>

</style>
