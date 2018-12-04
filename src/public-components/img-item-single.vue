<template>
    <div class="img-wraper">
        <img 
            class="imgItem" 
            :style="{'width':imgItemWidth+'rpx','height':imgItemWidth + 'rpx'}"
            :src="imgUrl" 
            @click.stop="previewImg"
        />
    </div>
</template>
<script>
    export default {
        props:{
            index:Number,
            imgUrls:Array,
            imgItemWidth:Number,
        },
        methods:{
            previewImg(){
               wx.previewImage({
                   current:this.imgUrl,
                   urls:this.imgUrls
               })
            }
        },
        computed:{
            imgUrl(){
                return this.imgUrls[this.index]
            }
        },
        mounted(){
            console.log(this.index,this.imgUrls,this.imgItemWidth,this.imgUrl)
        }
    }
</script>
<style lang="css" scoped>
    .imgItem{
        display:block;
        margin:5rpx;
    }
</style>