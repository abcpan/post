<template>
<div class="content">
    <div class="content__wrap">
        {{postContent}}
    </div><!--此处待处理-->
</div>
</template>
<script>
    export default {
        props:{
            postContent:String
        }
    }
</script>
<style lang="scss" scoped>
    .content{
        font-size: 32rpx;
        color: #333333;
        padding:10rpx 20rpx 0 30rpx;
        &__wrap{
            padding:0 60rpx 0 0;
            width:640rpx;
            display:-webkit-box;
            -webkit-box-orient:vertical;
            -webkit-line-clamp:4;
            overflow:hidden;
            text-overflow:ellipsis;
        }
    }
</style>