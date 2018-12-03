<template>
     <div class="location">
        <img class="location-icon" src="/static/position.png" mode="aspectFill" alt="">
        <span class="location-tip">深圳市南山区科技园</span>
        <span class="location-distance">一公里以内</span>
    </div>
</template>
<script>
    export default {

    }
</script>
<style lang="css" scoped>
    .location{
        font-size: 24rpx;
        color: #BBBBBB;
        padding:0 20rpx;
    }
    .location-icon{
        width:20rpx;
        height:28rpx;
        margin-right:30rpx;
    }
    .location-tip{
        margin-right:30rpx;
    }
</style>