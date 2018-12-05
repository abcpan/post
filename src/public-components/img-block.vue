<template>
    <div class="img-container" :style="{width:selfParrentWidth+'rpx'}">
        <imgItemSingle 
            :imgUrls="imgUrls" 
            v-for="(item,index) in imgUrls" 
            :key="index" 
            :index="index"
            :imgItemWidth="imgItemWidth"
        >
        </imgItemSingle>
    </div>
</template>
<script>
    import imgItemSingle from './img-item-single'
    export default {
        components:{
            imgItemSingle
        },
        props:{
            imgInfo:Object,
        },
        data() {
            return {
                selfParrentWidth:this.imgInfo.parrentWidth,
                imgUrls:this.imgInfo.imgUrls
            }
        },
        computed:{
            imgItemWidth() {
                return this.selfParrentWidth/this.palace -10
            },
            //确定是几宫格 4 就是田字格 其他9 宫格
            palace() {
               return this.imgUrls.length==4?2:3;
            }
        },
        mounted() {
            console.log(this.style,this.selfParrentWidth)
        }
    }
</script>
<style lang="css" scoped>
    .img-container{
        width:100%;
        display:flex;
        flex-wrap:wrap;
        justify-content:flex-start;
        margin:20rpx 0 20rpx 20rpx;
    }
</style>