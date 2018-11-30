<template>
    <div class="input-wrap">
        <input  class="input-area" type="text" placeholder="我也说一句">
        <div class="replay-block">
            <img  class="replay-icon" src="../../../assets/images/comment-icon.png"  mode="aspectFill" alt="">
            <span>99</span>
        </div>
        <div class="like-block">
            <img  class="like-icon" src="../../../assets/images/heart-default.png"  mode="aspectFill" alt="">
            <span>99</span>
        </div>
    </div>
</template>
<script>
    
</script>
<style lang="css" scoped>
    .input-wrap{
        height:98rpx;
        background:#eee;
        display:flex;
        align-items:center;
        font-size: 28rpx;
        color: #8E8E8E;
    }
    .input-area{
        width:370rpx;
        height:60rpx;
        display:block;
        outline:none;
        border-radius:8rpx;
        background: #FFFFFF;
        border-radius: 8rpx;
        margin-left:20rpx;
        box-sizing:border-box;
        padding:0 7rpx 0 7rpx;
    }
    .replay-block,.like-block{
        margin-left:60rpx;
        display:flex;
        align-items:center;
    }
    .replay-icon,.like-icon{
        width:44rpx;
        height:35rpx;
        margin-right:12rpx;
    }
</style>