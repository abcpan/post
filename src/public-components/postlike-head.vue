<template>
<div class="post__heading">
    <img class="heading-icon" src="/static/user.png" mode="aspectFill" alt="">
    <div class="heading-desc">
        <div class="desc-username">金木小公主</div>
        <div class="desc-time"><span class="time">刚刚</span>回复</div>
    </div>
    <div class="heading-focus">
        <div class="focus-button">
            关注
        </div>
    </div><!--按钮区域-->
</div>
</template>
<script>
    
</script>
<style lang="css" scoped>
      .post__heading{
        display:flex;
        height:90rpx;
    }
    .heading-icon{
        width:90rpx;
        height:90rpx;
        margin-left:13rpx;
    }
    .heading-desc{
        flex:1;
        margin-left:20rpx;
        display:flex;
        flex-direction:column;
        justify-content:center;
    }
    .desc-username{
        font-size: 28rpx;
        color: #8E8E8E;
    }
    .desc-time{
        font-size: 20rpx;
        color: #BBBBBB;
    }
    .time{
        margin-right:10rpx;
    }
    .heading-focus{
        width:150rpx;
        display:flex;
        flex-direction:column;
        justify-content:center;
    }
    .focus-button{
        width:120rpx;
        height:60rpx;
        line-height:60rpx;
        background:#FF5E5E;
        font-size: 28rpx;
        color: #FFFFFF;
        text-align:center;
        border-radius:8rpx;
    }
</style>
