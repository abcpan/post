<template>
    <div class="likelist">
        <div class="post-line"></div><!--间隔线-->
            <div class="post-like"><!--间隔线-->
                <div class="like-wrap">
                    <img  class="like-icon" src="/static/like-default.png" mode="aspectFill" alt="">
                    <img  class="user-icon" src="" alt="">
                    <img  class="user-icon" src="" alt="">
                    <img  class="user-icon" src="" alt="">
                </div>
            </div>
        <div class="post-line"></div><!--间隔线-->
        <div class="comment-info">
                <div class="info-tip">最新评论<span class="comment-num">6</span></div>
                <div class="info-sort">
                    从旧到新
                    <div class="arrow">
                        <div class="triangle"></div>
                        <div class="rect"></div>
                    </div>
                </div>
            </div>
    </div>
</template>
<script>
    
</script>
<style lang="css" scoped>
    .post-line{
            width:730rpx;
            height:2rpx;
            margin:0 auto;
            background: #DFDFDF;
        }
    .like-wrap{
        padding:0 10rpx 0 10rpx;
    }
    .like-icon,.user-icon{
        height:50rpx;
        width:50rpx;
        margin:10rpx 10rpx 10rpx 10rpx;
    }
    .user-icon{
        border-radius:50%;
        background:pink;
    }
    .comment-info{
        width:690rpx;
        margin:0 auto;
        font-size: 24rpx;
        color: #BBBBBB;
        display:flex;
        justify-content:space-between;
    }
    .comment-num{
        margin-left:30rpx;
    }
    .info-sort{
        display:flex;
        justify-content:center;
        align-items:center;
    }
    .arrow{
        width:20rpx;
    }
    .triangle{
        height:0;
        width:0;
        border-bottom:10rpx solid  #8E8E8E;
        border-right:10rpx solid transparent;
        border-left:10rpx solid transparent;
        margin:0 auto;
    }
    .rect{
        width:8rpx;
        height:15rpx;
        background:#8E8E8E;
        margin:0 auto;
    }
</style>