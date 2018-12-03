<template>
    <div class="bottom-input">
        <input  class="bottom-input__input-area" type="text" placeholder="我也说一句">
        <div class="bottom-input__reply">
            <img  class="reply-icon" src="/static/reply-icon.png"  mode="aspectFill" alt="">
            <span>99</span>
        </div>
        <div class="bottom-input__like">
            <img  class="like-icon" src="/static/heart-default.png"  mode="aspectFill" alt="">
            <span>99</span>
        </div>
    </div>
</template>
<script>
    
</script>
<style lang="scss" scoped>
    .bottom-input{
        height:98rpx;
        background:#eee;
        display:flex;
        align-items:center;
        font-size: 28rpx;
        color: #8E8E8E;
        &__input-area{
            width:370rpx;
            height:60rpx;
            outline:none;
            border-radius:8rpx;
            background: #FFFFFF;
            margin-left:20rpx;
            box-sizing:border-box;
            padding:0 20rpx 0 20rpx;
        }
        &__reply,&__like{
            margin-left:60rpx;
            display:flex;
            align-items:center;
            .reply-icon,.like-icon{
                width:44rpx;
                height:35rpx;
                margin-right:12rpx;
    }
        }
    }
</style>