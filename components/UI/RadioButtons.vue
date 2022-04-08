<template>
    <div class="flex flex-row">
        <div
            v-for="item in radioButtons"
            :id="item.id"
            :key="item"
            class="radio-btn"
        >
            <div v-if="item.chose">
                <div class="radio flex flex-row mr-[40px]" @click="radioClick(item.id)">
                    <div class="circle active">
                        <div class="ball active" />
                    </div>
                    {{ item.name }}
                </div>
            </div>
            <div v-else>
                <div class="radio flex flex-row mr-[40px]" @click="radioClick(item.id)">
                    <div class="circle ">
                        <div class="ball " />
                    </div>
                    {{ item.name }}
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                radioButtons: [
                    {
                        id: 0,
                        name: 'Ngày dương lịch',
                        chose: false,
                    },
                    {
                        id: 1,
                        name: 'Ngày âm lịch',
                        chose: true,
                    },
                ],
                value: null,
            };
        },
        methods: {
            radioClick(param) {
                this.radioButtons.forEach((item) => {
                    if (item.chose) {
                        item.chose = false;
                    }
                });
                this.radioButtons[param].chose = true;
                this.value = this.radioButtons[param].id;
            },
        },
    };
</script>
<style scoped>
    input[type='radio']:checked{
            color: red;
        }
    .radio-btn{
        display: flex;
        justify-content: center;
        color: #30323E;
        font-size: 16px;
        font-weight: 400;
        margin-bottom: 16px;
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
    }.circle.active{
        border: 2px solid #BF1014;
    }
    .ball.active{
        display: block;

    }
</style>
