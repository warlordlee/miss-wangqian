<template>
    <div class="main" @click="play">
        <el-carousel direction="vertical" :autoplay="false" indicator-position="none" ref="year"
                     :initial-index="index">
            <el-carousel-item>
                <common-container>
                    <img src="../assets/home.gif" class="full">
                </common-container>
            </el-carousel-item>
            <el-carousel-item>
                <common-container>
                    <img src="../assets/dsp.png" class="full">
                </common-container>
            </el-carousel-item>
            <el-carousel-item>
                <common-container>
                    <img src="../assets/wq.png" class="full">
                </common-container>
            </el-carousel-item>
            <el-carousel-item>
                <common-container>
                    <img src="../assets/dsp2.png" class="full">
                    <img src="../assets/girl.png" class="girl">
                </common-container>
            </el-carousel-item>
            <el-carousel-item>
                <common-container>
                    <img src="../assets/end.gif" class="full">
                </common-container>
            </el-carousel-item>
        </el-carousel>
        <div class="action"
             @click="handleClick">
            <img src="../assets/arr.png" style="width: 25px">
            <div>
                点击滚动
            </div>
        </div>
        <div class="music">
            <audio loop="loop" autoplay="autoplay" controls="controls" style="height: 1px" id="music-bg">
                <source src="../assets/music/girl.mp3" type="audio/mpeg">
            </audio>
        </div>
    </div>
</template>

<script>
    import commonContainer from '../components/commonContainer'
    export default {
        name: "home",
        components: {
            commonContainer
        },
        mounted() {
            let audio = document.getElementById("music-bg");
            audio.play();
            setTimeout(()=>{
                audio.play()
            },200)
        },
        data() {
            return {
                index: 0,
            }
        },
        methods: {
            handleClick() {
                this.$refs.year.next();
                let audio = document.getElementById("music-bg");
                audio.play();
            },
            play(){
                let audio = document.getElementById("music-bg");
                audio.play();
            }
        }
    }
</script>

<style scoped lang="less">
    .music{
        position: absolute;
        top: 0;
        right: 0;
        opacity: 0.1;
    }
</style>
