<template>
    <div class="img-wraper">
        <img 
            class="imgItem" 
            :style="{'width':imgItemWidth+'rpx','height':imgItemWidth+additon+ 'rpx'}"
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
            single:Boolean
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
            },
            // 确定是否单图显示,如果是单图显示  就为高度加100
            additon(){
                if(this.single===true && this.imgUrls.length==1){
                    return 100
                }else{
                    return 0
                }
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