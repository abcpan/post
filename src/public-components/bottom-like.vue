<template>
<div class="bottom__like">
    <div class="like">
        <img  class="like-img" src="/static/heart-default.png"  alt="">
        <div class="like-num">123456</div>
    </div><!--投票区域-喜欢区域-->
    <div class="line"></div>
    <div class="reply">
        <img class="reply-img" src="/static/reply-icon.png"   alt=""/>
        <div class="reply-num">123456</div>
    </div><!--投票区域-回复区域-->
</div>
</template>
<script>
    
</script>
<style lang="css">
    .bottom__like{
        margin-top:40rpx;
        height:90rpx;
        border-top:2rpx solid #DFDFDF;
        display:flex;
        align-items:center;
    }
    .line{
        width:4rpx;
        height:45rpx;
        background:#DFDFDF;
    }
    .like,.reply{
        flex:1;
        display:flex;
        justify-content:center;
        align-items:center;
        font-size: 28rpx;
        color: #8E8E8E;
    }
    .like-img,.reply-img{
        height:42rpx;
        width:40rpx;
        display:block;
    }
    .like-num,.reply-num{
        margin-left:20rpx;
    }
</style>
