<template>
    <div class="img-container" :style="{width:parrentWidth+'rpx'}">
        <imgItemSingle 
            :imgUrls="imgUrls" 
            v-for="(item,index) in imgUrls" 
            :key="index" 
            :index="index"
            :imgItemWidth="imgItemWidth"
            :single="single"
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
                parrentWidth:this.imgInfo.parrentWidth,
                imgUrls:this.imgInfo.imgUrls,
                single:this.imgInfo.single
            }
        },
        computed:{
            imgItemWidth() {
                if(this.single && this.imgUrls.length==1){ //传入一张图片 且确定为single显示 为一宫格 否则 按照常规处理
                    return 358
                }else{  
                   return this.parrentWidth/this.palace -10 
                }
                
            },
            //确定是几宫格4就是田字格其他9宫格
            palace() {
                return this.imgUrls.length==4?2:3;
            }
        },
        mounted() {
            console.log(this.selfParrentWidth)
        }
    }
</script>
<style lang="css" scoped>
    .img-container{
        width:100%;
        display:flex;
        flex-wrap:wrap;
        justify-content:flex-start;
        margin:20rpx auto;
    }
</style>