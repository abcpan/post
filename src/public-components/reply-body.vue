<template>
    <div class="reply-body">
        <div class="content-wrap">
            <div class="content__main">{{replyContent.text}}</div>
            <imgBlock :imgInfo="imgInfo"></imgBlock>
        </div>
        <div class="from">
            <span class="from-tip">原贴:</span>
            <span class="from-post">{{postName}}</span>
        </div>
    </div>
</template>
<script>
import imgBlock from './img-block'
export default {
    props:{
        postName:String,
        replyContent:Object
    },
    data() {
        return {
            imgUrls:this.replyContent.imgUrls
        }
    },
    components:{
        imgBlock
    },
    computed:{
        imgInfo(){
            let imgUrls  = this.imgUrls
            let parrentWidth = 670
            let single = true
            return Object.assign({},{imgUrls,parrentWidth,single})
        }
    }
}
</script>
<style lang="css" scoped>
.reply-body{
    background: #FFFFFF;
    border-radius:10rpx;
    padding:20rpx;
}
.body__inline{
    height:2rpx;
    width:100%;
    background:#DFDFDF;
    margin:30rpx 0;
}
.content-wrap{
   width:622rpx;
}
.content-wrap::after{
    content:"";
    display:block;
    height:2rpx;
    width:100%;
    background:#DFDFDF;
    margin:30rpx 0;
}
.content__main{
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp:4;
    overflow: hidden;
    text-overflow:ellipsis;
    font-size:32rpx;
    color: #333333;
}
.from{
    font-size: 32rpx;
    color: #333333;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp:1;
    overflow: hidden;
    text-overflow:ellipsis;
}
.from-tip{
    margin-right:10rpx;
}
</style>