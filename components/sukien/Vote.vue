<template>
    <div class="bg-white p-6 mr-4 flex flex-col w-[680px] rounded-[4px] mb-6">
        <span class="text-[#252733] text-[16px] font-bold mb-6">Nội dung bình chọn</span>
        <div>
            <div
                v-for="item in items"
                :id="item.id"
                :key="item"
            >
                <div v-if="item.chose">
                    <div class="flex flex-row justify-between border border-[#F9E8CB] rounded-[4px] h-[45px] mt-4 p-3" @click="selected(item.id)">
                        <span>{{ item.name }}</span>
                        <div class="w-[24px] h-[24px] border border-[#E79000] rounded-full relative">
                            <div class="ball active" />
                        </div>
                    </div>
                </div>
                <div v-else>
                    <div class="flex flex-row justify-between border border-[#F9E8CB] rounded-[4px] h-[45px] mt-4 p-3" @click="selected(item.id)">
                        <span>{{ item.name }}</span>
                        <div class="w-[24px] h-[24px] border border-[#A3A4A9] rounded-full relative">
                            <div class="ball" />
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <button class="border border-[#E79000] rounded-[4px] h-[40px] mt-4" @click="dialogFormVisible = true">
            <span class="text-[16px] text-[#E79000] font-bold">
                <i class="el-icon-circle-plus" />
                Đề cử
            </span>
        </button>
        <el-dialog :visible.sync="dialogFormVisible">
            <div class="bg-[#fff] flex flex-col mx-auto z-100 py-4">
                <div class="mx-auto mt-[26px]">
                    <span class=" text-[#000] text-[24px] font-bold">Đề cử</span>
                </div>
                <div class="mx-auto  mt-3">
                    <span class=" text-[#75767E] text-4">Tạo tài khoản cho các user là thành viên</span>
                </div>
                <div class="flex flex-col mx-auto mt-8 w-11/12">
                    <span class=" text-[#252733] text-[16px] mt-8">Nội dung đề cử</span>
                    <div class=" flex flex-row justify-between mt-2 ">
                        <input type="text" class=" w-11/12 rounded-[4px] border border-[#F0E7DA] px-4 py-[11px] h-12" placeholder="Nhập nội dung đề cử">
                        <i class="el-icon-success" />
                    </div>
                    <span class="text-[#252733] text-[16px] mt-8">Lý do đề cử</span>
                    <textarea class=" mt-2 rounded-[4px] border border-[#F0E7DA]  h-[168px] px-4 py-[11px]" placeholder="Lý do nhập đề cử" />
                </div>
                <div class="flex flex-row justify-center mt-8">
                    <button @click="dialogFormVisible = false" class=" h-[48px] w-4/12 rounded-[4px] text-[#BF1014] text-[18px] font-bold border border-[#BF1014] mr-4">
                        Hủy bỏ
                    </button>
                    <button @click="dialogFormVisible = false" class="h-[48px] w-4/12 rounded-[4px] text-[#fff] text-[18px] font-bold bg-[#BF1014]">
                        Đề cử
                    </button>
                </div>
            </div>
        </el-dialog>
        <button :class="{button: isActive}" class="bg-[#A3A4A9] rounded-[4px] h-[40px] mt-6 text-[16px] text-[#fff] font-bold" @click="vote()">
            Bình chọn
        </button>
    </div>
</template>
<script>
    export default {
        props: [
            'items',
        ],
        data() {
            return {
                dialogFormVisible: false,
                isActive: false,
                idChose: null,
            };
        },
        methods: {
            selected(param) {
                this.isActive = true;
                this.idChose = param;
                this.$emit('selected', param);
            },
            vote() {
                if (!this.isActive) {
                    return 0;
                }
                this.$emit('vote', this.idChose);
                this.$emit('isVote', true);
            },
            addDeCu() {
            },
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
    i.el-icon-success {
        color: #BF1014;
        margin: auto 0;
        font-size: 20px;
    }
    .button{
        background-color: #BF1014;
    }
    input:focus, textarea:focus{
        outline: none;
    }
</style>
