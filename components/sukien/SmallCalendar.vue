<template>
    <div class=" w-[416px] h-[388px] bg-white pt-4">
        <!-- <div class=" flex justify-between pt-4">
            <div class=" w-[40px] h-[40px] rounded-[6px] shadow-xl text-[20px] flex justify-center"><i class="el-icon-arrow-left"></i></div>
            <div class=" font-bold text-[16px] text-[#000323] leading-10 mx-auto">Tháng 10</div>
            <div class=" w-[40px] h-[40px] rounded-[6px] shadow-xl text-[20px] flex justify-center"><i class="el-icon-arrow-right"></i></div>
        </div> -->
        <div class=" flex flex-row justify-between h-10">
            <div class=" w-10 h-10 rounded-[6px] shadow-xl ml-4 flex flex-row justify-center">
                <i class="el-icon-arrow-left" />
            </div>
            <div class=" leading-10 font-bold text-[#000323] text-[16px]">
                Tháng 10
            </div>
            <div class=" w-10 h-10 rounded-[6px] shadow-xl mr-4 flex flex-row justify-center">
                <i class="el-icon-arrow-right" />
            </div>
        </div>
        <!-- <div class=" mt-3 ml-[33px] mr-[33px] grid grid-cols-7 justify-between tetx-[14px] text-[#252733]" /> -->
        <div class=" ml-[33px] mr-[33px] mt-6 grid grid-cols-7 gap-4 justify-between">
            <div class="flex flex-row justify-center">
                HAI
            </div>
            <div class="flex flex-row justify-center">
                BA
            </div>
            <div class="flex flex-row justify-center">
                TƯ
            </div>
            <div class="flex flex-row justify-center">
                NĂM
            </div>
            <div class="flex flex-row justify-center">
                SÁU
            </div>
            <div class="flex flex-row justify-center">
                BẢY
            </div>
            <div class="flex flex-row justify-center">
                CN
            </div>
            <div>
                <div class="ngayduong">
                    28
                </div>
                <div class="ngayam">
                    30
                </div>
            </div>
            <div>
                <div class="ngayduong">
                    29
                </div>
                <div class="ngayam">
                    31
                </div>
            </div>
            <div>
                <div class="ngayduong">
                    30
                </div>
                <div class="ngayam">
                    1/10
                </div>
            </div>
            <div>
                <div class="ngayduong">
                    31
                </div>
                <div class="ngayam">
                    2
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    1
                </div>
                <div class="ngayam">
                    3
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    2
                </div>
                <div class="ngayam">
                    4
                </div>
            </div>
            <div>
                <div class="ngayduong active red">
                    3
                </div>
                <div class="ngayam">
                    5
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    4
                </div>
                <div class="ngayam">
                    6
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    5
                </div>
                <div class="ngayam">
                    7
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    6
                </div>
                <div class="ngayam">
                    8
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    7
                </div>
                <div class="ngayam">
                    9
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    8
                </div>
                <div class="ngayam">
                    10
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    9
                </div>
                <div class="ngayam">
                    11
                </div>
            </div>
            <div>
                <div class="ngayduong active red">
                    10
                </div>
                <div class="ngayam">
                    12
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    11
                </div>
                <div class="ngayam">
                    13
                </div>
            </div>
            <div>
                <div class="ngayduong active prime relative">
                    12
                    <div class=" absolute left-8">
                        <img src="@/static/img/kyniem.png" alt="">
                    </div>
                </div>
                <div class="ngayam">
                    14
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    13
                </div>
                <div class="ngayam">
                    15
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    14
                </div>
                <div class="ngayam">
                    16
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    15
                </div>
                <div class="ngayam">
                    17
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    16
                </div>
                <div class="ngayam">
                    18
                </div>
            </div>
            <div>
                <div class="ngayduong active red">
                    17
                </div>
                <div class="ngayam">
                    19
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    18
                </div>
                <div class="ngayam">
                    20
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    19
                </div>
                <div class="ngayam">
                    21
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    20
                </div>
                <div class="ngayam">
                    22
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    21
                </div>
                <div class="ngayam">
                    23
                </div>
            </div>
            <div>
                <div class="ngayduong active">
                    22
                </div>
                <div class="ngayam">
                    24
                </div>
            </div>
            <div>
                <div>
                    <div class=" mx-auto ngayduong active supperred relative bg-[#F9E8E8] rounded-full w-6">
                        23
                        <div class=" bg-[#BF1014] w-[5px] h-[5px] rounded-full absolute left-5" />
                    </div>
                </div>
                <div class="ngayam">
                    25
                </div>
            </div>
            <div>
                <div class="ngayduong">
                    24
                </div>
                <div class="ngayam">
                    26
                </div>
            </div>
            <div>
                <div class="ngayduong">
                    25
                </div>
                <div class="ngayam">
                    27
                </div>
            </div>
            <div>
                <div class="ngayduong">
                    26
                </div>
                <div class="ngayam">
                    28
                </div>
            </div>
            <div>
                <div class="ngayduong">
                    27
                </div>
                <div class="ngayam">
                    29
                </div>
            </div>
            <div>
                <div class="ngayduong">
                    28
                </div>
                <div class="ngayam">
                    30
                </div>
            </div>
            <div>
                <div class="ngayduong">
                    29
                </div>
                <div class="ngayam">
                    1
                </div>
            </div>
            <div>
                <div class="ngayduong">
                    30
                </div>
                <div class="ngayam">
                    2
                </div>
            </div>
            <div>
                <div class="ngayduong">
                    1
                </div>
                <div class="ngayam">
                    3
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
    };
</script>
<style scoped>
    .el-icon-arrow-left, .el-icon-arrow-right {
        font-weight: bold;
        color: #000323;
        line-height: 40px;
        margin: auto 0;
    }
    .ngayduong{
        color: #A3A4A9;
        font-size: 14px;
        display: flex;
        flex-direction: row;
        justify-content: center;
    }
    .ngayduong.active{
        color: #191B28;
    }
    .ngayduong.active.red{
        color: #BF1014;
    }
    .ngayduong.active.prime{
        color: #E79000;
        font-weight: bold;
    }
    .ngayduong.active.supperred{
        color: #BF1014;
        font-weight: bold;
    }
    .ngayam{
        color: #75767E;
        font-size: 10px;
        display: flex;
        flex-direction: row;
        justify-content: center;
    }
</style>
