<template>
     <div class="location">
        <img class="location-icon" src="/static/position.png" mode="aspectFill" alt="">
        <span class="location-tip">{{location.coordinate}}ss</span>
        <span class="location-distance">{{location.distance}}</span>
    </div>
</template>
<script>
    export default {
        props:{
            location:Object
        }
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