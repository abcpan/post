<template>
<div class="content">
    <div class="content__wrap">
        {{postContent}}
    </div><!--此处待处理-->
    <div class="content__reply">
        <p>【支持】陪孩子和老公出去玩</p>
        <p>【支持】陪孩子和老公出去玩</p>
    </div>
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
        &__reply{
            margin:50rpx 0 0 10rpx;
        }
    }
</style>