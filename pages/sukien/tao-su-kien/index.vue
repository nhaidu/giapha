<template>
    <div class="w-[1032px] mx-auto flex flex-col">
        <div class="flex flex-row justify-items-start mb-[24px] w-[1034px] mx-auto">
            <div class="inline-block">
                <span class="text-[16px] text-[#606266] mr-[13px]">Trang chủ</span>
                <i class="el-icon-arrow-right" />
                <span class="text-[16px] text-[#606266] ">Sự kiện</span>
                <i class="el-icon-arrow-right" />
                <span class="text-[16px] text-[#606266] font-bold">Tạo sự kiện</span>
            </div>
        </div>
        <div class="flex flex-row justify-between mb-[30px] mt-6 ">
            <div class="bg-white p-6 mr-4 flex flex-col w-[680px] rounded-[4px] mb-6">
                <span class=" text-[#252733] text-[16px] mb-2">Tạo sự kiện</span>
                <input type="text" placeholder="Nhập tên sự kiện" class="mb-4 w-[632px] h-[48px] border border-[#FDF4E6] rounded-[4px]">
                <span class=" text-[#252733] text-[16px] mb-4">Thời gian bắt đầu</span>
                <RadioButtons />
                <div class="flex flex-row">
                    <el-time-select
                        v-model="house"
                        :picker-options="{
                            start: '08:30',
                            step: '00:15',
                            end: '18:30'
                        }"
                        placeholder="Chọn giờ"
                    />
                    <div class="w-[10px]" />
                    <el-date-picker
                        v-model="date"
                        type="date"
                        placeholder="Chọn ngày"
                    />
                </div>
                <div class="mt-4">
                    <span class="text-[#30323E] text-[14px]">Ngày âm lịch</span>
                </div>
                <div class="mt-4 mb-4">
                    <span class="text-[16px] text-[#252733]">Thời gian kết thúc</span>
                </div>
                <RadioButtons />
                <div class="flex flex-row">
                    <el-time-select
                        v-model="house"
                        :picker-options="{
                            start: '08:30',
                            step: '00:15',
                            end: '18:30'
                        }"
                        placeholder="Chọn giờ"
                    />
                    <div class="w-[10px]" />
                    <el-date-picker
                        v-model="date"
                        type="date"
                        placeholder="Chọn ngày"
                    />
                </div>
                <div class="mt-4">
                    <span class="text-[#30323E] text-[14px]">Ngày âm lịch</span>
                </div>
                <div class="mt-4">
                    <span class="text-[#252733] text-[16px]">Loại sự kiện</span>
                </div>
                <div class="mt-2">
                    <SelectOption />
                </div>
                <div class="mt-4">
                    <span class="text-[#252733] text-[16px]">Mô tả ngắn</span>
                </div>
                <div class="mt-2">
                    <textarea class=" rounded-[4px] border border-[#F0E7DA] w-[632px] h-[80px] py-[11px] px-[16px]" placeholder="Nhập mô tả ngắn về sự kiện" />
                </div>
                <div class="mt-4">
                    <span class="text-[#252733] text-[16px]">Nội dung sự kiện</span>
                </div>
                <div class="mt-2">
                    <textarea class=" rounded-[4px] border border-[#F0E7DA] w-[632px] h-[160px] py-[11px] px-[16px]" placeholder="Nhập mô tả ngắn về sự kiện" />
                </div>
                <div class="mt-4">
                    <span class="text-[#252733] text-[16px]">Trách nghiệm</span>
                </div>
                <div class="mt-2">
                    <input type="text" class=" rounded-[4px] border border-[#F0E7DA] w-[632px] h-[48px] py-[11px] px-[16px]" placeholder="Nhập trách nghiệm khi tham gia sự kiện">
                </div>
            </div>
            <div class="bg-white p-6 mr-4 flex flex-col w-[328px] rounded-[4px] mb-6">
                <div>
                    <span class="text-[16px] text-[#252733]">Đối tượng tham gia</span>
                </div>
                <div class="mb-2">
                    <SelectOption />
                </div>
                <div class="mt-4">
                    <span class="text-[16px] text-[#252733]">Lặp lại</span>
                </div>
                <div class="mb-2">
                    <SelectOption />
                </div>
                <div class="mt-4">
                    <span class="text-[16px] text-[#252733]">Nhắc trước</span>
                </div>
                <div class="mb-2">
                    <SelectOption />
                </div>
                <div class="mt-4">
                    <span class="text-[16px] text-[#252733]">Nhắc trước</span>
                </div>
                <div class="w-[280px] relative h-[214px] border border-[#FDF4E6] rounded-[4px] uploadCover">
                    <input type="file" class="opacity-0 absolute top-0 left-0 w-[280px] h-[214px]">
                    <div class="flex flex-col justify-center items-center absolute upload">
                        <i class="el-icon-camera-solid top-0 left-0" />
                        <span>Tải ảnh cover sự kiện</span>
                    </div>
                </div>
                <div class="mt-4">
                    <span class="text-[16px] text-[#252733]">Ảnh sự kiện</span>
                </div>
                <div class="mt-[8px]">
                    <button class="border border-[#F5D399] h-[48px] w-[280px] rounded-[4px] text-[#E79000] text-[16px] bg-[#FDF4E6] text-center " @click="uploadFile()">
                        <i class="el-icon-folder-add" />
                        Tải file lên (.jpeg, .png,.pdf)
                    </button>
                    <input ref="inputfile" type="file" class="opacity-0">
                </div>
                <div class="mt-4">
                    <span class="text-[16px] text-[#252733]">Tài liệu sự kiện</span>
                </div>
                <div class="mt-[8px]">
                    <button class="border border-[#F5D399] h-[48px] w-[280px] rounded-[4px] text-[#E79000] text-[16px] bg-[#FDF4E6] text-center " @click="uploadFile()">
                        <i class="el-icon-folder-add" />
                        Tải file lên (.docx, .pdf, .xlsx, .xls)
                    </button>
                    <input ref="inputfile" type="file" class="opacity-0">
                </div>
            </div>
        </div>
        <div class="mt-6 mx-auto mb-9">
            <button class=" w-[382px] h-[48px] text-[18px] text-white font-bold bg-[#A3A4A9]">
                Tạo sự kiện
            </button>
        </div>
    </div>
</template>
<script>
    import RadioButtons from '@/components/UI/RadioButtons.vue';
    import SelectOption from '../../../components/UI/SelectOption.vue';

    export default {
        components: {
            RadioButtons,
            SelectOption,
        },
        data() {
            return {
                house: null,
                date: null,
            };
        },
        methods: {
            uploadFile() {
                this.$refs.inputfile.click();
            },
        },
    };
</script>
<style>
    input{
        padding-left: 15px;
    }
    input:focus {
        outline: none !important;
    }
    textarea:focus, textarea{
        outline: none;
        resize: none;
    }
    .el-icon-camera-solid{
        font-size: 50px;
        color: #BF1014;
    }
    .upload{
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
    .uploadCover{
        cursor: pointer;
    }
</style>
