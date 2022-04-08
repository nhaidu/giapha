<template>
    <div class="mt-[8px] relative">
        <div ref="popuptitle" class=" mt-[8px] rounded-4 border h-[48px] border-[#FDF4E6] px-[16px] py-[11px] flex flex-row justify-between" @click="openPopup()">
            <span v-if="value === null" class="text-[16px] text-[#A3A4A9]">Chọn Tỉnh/TP</span>
            <span v-else class="text-[16px] text-[#A3A4A9]"> {{ value }} </span>
            <i class="el-icon-arrow-up" />
        </div>
        <div ref="popup" class="selectoption bg-[#fff] w-full hidden absolute top-0">
            <div class="h-[42px] pl-[24px] text-[18px] font-bold leading-[42px]">
                Tỉnh/TP
            </div>
            <div class=" border-b border-[#F5F5F6]" />
            <div
                v-for="item in items"
                :id="item.id"
                :key="item"
            >
                <div v-if="item.chose">
                    <div class="selected active my-2" @click="selected(item.id)">
                        <span class=" h-[50px] w-full leading-[50px] pl-[24px] text-[14px] text-[#BF1014]">{{ item.name }}</span>
                        <div class="my-auto">
                            <div ref="datecircle2" class="circle active">
                                <div ref="dateball2" class="ball active" />
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                items: [
                    {
                        id: 0,
                        name: 'Hà Nam',
                        chose: false,
                    },
                    {
                        id: 1,
                        name: 'Hà Nội',
                        chose: false,
                    },
                    {
                        id: 2,
                        name: 'Hà Nội',
                        chose: false,
                    },
                ],
                value: null,
                status: 0,
            };
        },
        methods: {
            selected(param) {
                this.items.forEach((item) => {
                    if (item.chose) {
                        item.chose = false;
                    }
                });
                this.items[param].chose = true;
                this.value = this.items[param].name;
                this.$refs.popup.classList.add('hidden');
                this.$refs.popuptitle.classList.remove('hidden');
            },
            openPopup() {
                if (this.status === 0) {
                    this.$refs.popup.classList.remove('hidden');
                    this.$refs.popuptitle.classList.add('hidden');
                    this.status = 1;
                } else {
                    this.$refs.popup.classList.add('hidden');
                    this.$refs.popuptitle.classList.remove('hidden');
                    this.status = 0;
                }
            },
        },
    };
</script>
<style scoped>
    .selectoption{
        box-shadow: 0px 10px 15px -3px rgba(0, 0, 0, 0.1), 0px 4px 6px -2px rgba(0, 0, 0, 0.05);
        border-radius: 8px;
    }
    .circle{
        margin-right: 16px;
        width: 24px;
        height: 24px;
        border: 2px solid #BABBBE;
        border-radius: 50px;
        position: relative;
        background-color: #ffffff;
    }
    .ball{
        display: none;
        width: 14px;
        height: 14px;
        background-color: #BF1014;
        border-radius: 50px;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
    .circle.active{
        border: 2px solid #BF1014;
    }
    .ball.active{
        display: block;

    }
    .selected{
        display: flex;
        justify-content: space-around;
        margin: auto;
        justify-items: center;
    }
    .selected:hover{
        background-color: #F9E8E8;
    }
    .selected.active{
        background-color: #F9E8E8;
    }
</style>
