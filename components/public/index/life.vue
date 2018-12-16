<template>
    <div class="m-life">
        <el-row>
            <el-col :span="14">
                <slider />
            </el-col>
            <el-col :span="4">
                <img src="http://p0.meituan.net/codeman/e473bb428f070321269b23370ff02ba956209.jpg" style="width:150px;height:240px;margin:10px 10px 10px 0">
                <!-- <div class="m-life-pic"></div> -->
            </el-col>
            <el-col :span="6">
                登录注册
            </el-col>
        </el-row>
        <el-row>
            <el-col :span="7">
                <img src="http://p1.meituan.net/codeman/8cce56c467a17e04f3094d1e455462a0132772.png" style="background-size: 270px;width:270px;height:165px;margin:0 10px 0 10px">
                <!-- <div class="m-life-hotel"></div> -->
            </el-col>
            <el-col :span="7">
                <!-- 涨姿势 -->
                <img src="http://p1.meituan.net/codeman/16442c19da1f1c4544f794e29d99c92051716.jpg" style="background-size: 270px;width:270px;height:165px;margin:0 10px 0 10px">
                 <!-- <div class="m-life-music"></div> -->
            </el-col>            
            <el-col :span="4">
                <!-- 我是商家 -->
                <img src="http://p1.meituan.net/codeman/5b21cddb4bb1cbc3a9c3bce0f726c75940469.jpg" style="background-size: 150px;width:150px;height:165px;margin:0 10px 0 10px">
                <!-- <div class="m-life-coop"/> -->
            </el-col>
            <el-col :span="6">
                <!-- 美团二维码 -->
                <div class="m-life-downapp">
                <img 
                    src="//s1.meituan.net/bs/fe-web-meituan/60ac9a0/img/download-qr.png" 
                    alt="下载APP">
                <p>美团APP手机版</p>
                <h4><span class="red">1元起</span><em class="gary">吃喝玩乐</em></h4>
                </div>                
            </el-col>
        </el-row>
    </div>

</template>
<script>
    import Slider from './slider.vue'
    export default{
        components: {
            Slider
        }

    }
</script>
<style lang="scss">
    @import '@/assets/css/index/life.scss'
</style>