<template>
    <div class=" w-screen bg-[#191B28] flex flex-col p-10">
        <div class="flex flex-row justify-between">
            <div class="hover:opacity-75">
                <i class="el-icon-back" />
            </div>
            <div class="flex flex-row">
                <div class="hover:opacity-75">
                    <i class="el-icon-delete-solid" />
                </div>
                <div class="hover:opacity-75">
                    <i class="el-icon-download" />
                </div>
            </div>
        </div>
        <div class="flex flex-row mb-[55px] mt-[100px] mx-auto">
            <div class="my-auto mr-8 bg-[#474953] rounded-full w-[50px] h-[50px] relative cursor-pointer hover:opacity-75">
                <i class="el-icon-d-arrow-left" />
            </div>
            <img src="@/static/img/photofull.png" class="w-[856px] h-auto">
            <div class="my-auto ml-8 bg-[#474953] rounded-full w-[50px] h-[50px] relative cursor-pointer hover:opacity-75">
                <i class="el-icon-d-arrow-right" />
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        layout: 'auth',
    };
</script>
<style>
    .el-icon-download, .el-icon-back, .el-icon-delete-solid, .el-icon-d-arrow-left, .el-icon-d-arrow-right {
        color: white;
        font-size: 20px;
        font-weight: bold;
    }
    body::-webkit-scrollbar {
        width: 1px;
    }
    .el-icon-d-arrow-left, .el-icon-d-arrow-right {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);;
    }
    .el-icon-delete-solid{
        margin-right: 20px;
    }
    body{
        overflow-x: hidden;
    }
</style>
