<template>
    <div class="resgister">
        <img src="@/static/img/bgtop.png" alt="">
        <div class="resgister-body">
            <div class="content">
                <div class="content-left">
                    <div class="img-dragon">
                        <img src="@/static/img/dragon.png" alt="">
                    </div>
                </div>
                <div class="content-right">
                    <el-row class="text">
                        <div class="check">
                            <span class="text-1">Bạn chưa có tài khoản?</span>
                            <span class="text-2" @click="register()">Đăng ký</span>
                        </div>
                    </el-row>
                    <el-row class="detail">
                        <img src="@/static/img/forget.png" alt="">
                    </el-row>
                    <el-row v-model="code" class="text-sub">
                        <p class="sub">
                            Nhập mã email/số điện thoại, chúng tôi sẽ gửi mật khẩu mới vào email/số điện thoại của bạn
                        </p>
                    </el-row>
                    <el-row>
                        <el-input v-model="sdt" placeholder="Email / Số điện thoại" />
                    </el-row>
                    <el-row>
                        <el-button class="btn-5" @click="submit()">
                            Xác nhận
                        </el-button>
                    </el-row>
                </div>
            </div>
        </div>
        <img src="@/static/img/bgbottom.png" alt="">
    </div>
</template>

<script>
    export default {
        layout: 'auth',
        data() {
            return {
                code: '',
                radio: '',
                sdt: '',
                pass: '',
            };
        },
        methods: {
            submit() {
                this.$router.push('/login');
            },
            register() {
                this.$router.push('/register');
            },
        },
    };
</script>

<style scoped>
* {
    margin: 0;
    padding: auto;
    list-style: none;
    text-decoration: none;
}

.resgister {
    background-color: #980C0F;
    max-width: 1440px;
    margin: 0 auto;
}

.resgister-body {}

.content {
    margin: 69px auto;
    width: 856px;
    height: 600px;
    display: flex;
}

.content-left {
    border-top-left-radius: 20px;
    border-bottom-left-radius: 20px;
    display: flex;
    justify-content: center;
    height: 600px;
    width: 328px;
    background-color: #BF1014;
}

.img-dragon {
    margin: 167px auto;
}

.content-right {
    border-top-right-radius: 20px;
    border-bottom-right-radius: 20px;
    background-color: #FEF9F2;
    width: 528px;
}

.text {
    margin-bottom: 94px;
    margin-top: 24px;
}

.check {
    float: right;
    padding-right: 48px;
}

.text-1 {
    font-family: 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    color: #75767E;
    font-weight: 400;
    font-size: 16px;
    line-height: 26px;
    margin-right: 8px;
}

.text-2 {
    color: #E79000;
    font-family: 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    font-weight: bold;
    font-size: 18px;
    line-height: 26px;
}

.detail {
    display: flex;
    justify-content: center;
    margin-bottom: 30px;
}

.text-sub.el-row {
    text-align: center;
    padding: 0 48px;
    margin-bottom: 40px;
}

.sub {
    font-size: 16px;
    font-weight: 400;
    color: #75767E;
}
.radio-btn{
    display: flex;
    justify-content: center;
    color: #30323E;
    font-size: 16px;
    font-weight: 400;
    margin-bottom: 16px;
}
.radio-2{
    margin-left: 40px;
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
.el-input {
    margin-left: 48px;
    width: 432px;
    height: 48px;
    color: A3A4A9;
    font-weight: 700;
    font-size: 16px;
    font-family: 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    line-height: 26px;
    margin-bottom: 16px;
}

.btn-5 {
    margin-top: 24px;
    margin-left: 48px;
    width: 432px;
    height: 48px;
    color: white;
    font-weight: 700;
    font-size: 18px;
    background-color: #BF1014;
    font-family: 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    line-height: 26px;
    margin-bottom: 16px;
}

.tex-6 {
    text-align: right;
}

.text-6 {
    color: #474953;
    font-weight: normal;
    font-size: 16px;
    line-height: 26px;
    font-family: 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-right: 48px;
}
</style>
