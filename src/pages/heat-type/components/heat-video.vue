<template>
     <div class="heat-video">
            <div class="video__heading">
                <img class="heading-icon" src="../../../assets/images/icon.png" mode="aspectFill" alt="">
                <div class="heading-desc">
                    <div class="desc-username">匿名</div>
                    <div class="desc-time"><span class="time">刚刚</span>回复</div>
                </div>
                <div class="heading-nav"><img class="nav-img" src="../../../assets/images/path.png" alt="" mode="aspectFill" ></div>
            </div>
            <div class="video-body">
                <div class="video-title">
                    宝宝两岁半，就喜欢吃糖，一出门就要买糖吃
                    一天吃好几根棒棒糖，怎么办宝宝两岁半，就
                    喜欢吃糖，一出门就要买糖吃一天吃好几根棒
                    棒糖，怎么办？怎么办？我么秒内阿胶方法in哦么恶疾诶恶疾ii
                </div><!--此处待处理-->
                  <video class="video-source" :src="videoUrl"  enable-danmu danmu-btn controls></video>
            </div><!--热议视频的身体-->
             <div class="video__vote">
                <div class="vote-like">
                    <img  class="like-img" src="../../../assets/images/heart.png"  alt="">
                    <div class="like-num">123456</div>
                </div><!--投票区域-喜欢区域-->
                <div class="vote-line"></div>
                <div class="vote-reply">
                    <img class="reply-img" src="../../../assets/images/comment-icon.png"   alt=""/>
                    <div class="reply-num">123456</div>
                </div><!--投票区域-回复区域-->
            </div><!--投票区域-->
        </div><!--热议卡片-->
</template>
<script>
    export default {
        data() {
            return {
                videoUrl:""
            }
        }
    }
</script>
<style lang="css" scoped>
    .heat-video{
        width:730rpx;
        margin:0 auto;
        background: #FFFFFF;
        border-radius: 46.85rpx 10rpx 10rpx 10rpx;
        margin-bottom:20rpx;
    }
    .video__heading{
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
    .heading-nav{
        width:70rpx;
        display:flex;
        justify-content:center;
    }
    .nav-img{
        width:15rpx;
        height:29rpx;
        transform:rotate(90deg);
        margin-top:10rpx;
    }
    .video-body{
        margin-top:10rpx;
        width:690rpx;
        margin:0 auto;
    }
    .video__content{
        font-size: 32rpx;
        color: #333333; 
    }
    .video-title{
        width:640rpx;
        display:-webkit-box;
        -webkit-box-orient:vertical;
        -webkit-line-clamp:2;
        overflow:hidden;
        text-overflow:ellipsis;
        font-size: 32rpx;
        color: #333333;
    }
    .video-source{
        margin:0 auto;
        margin-top:20rpx;
        width:670rpx;
        height:374rpx;
    }
    .video__vote{
        margin-top:40rpx;
        height:90rpx;
        border-top:2rpx solid #DFDFDF;
        display:flex;
        align-items:center;
    }
    .vote-line{
        width:4rpx;
        height:45rpx;
        background:#DFDFDF;
    }
    .vote-like,.vote-reply{
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
    .like-status{}
    .like-status-word{
        margin-left:20rpx;
        font-size: 24rpx;
        color: #FB5E62;
        line-height:33rpx;
    }
    .like-status-bar{
        height:9rpx;
        width:200rpx;
        background: #FB5E62;
    }
    .reply-status{}
    .reply-status-word{
        margin-right:20rpx;
        font-size: 24rpx;
        color: #62C5C8;
        line-height:33rpx;
    }
    .reply-status-bar{
        height:9rpx;
        width:384rpx;
        background:#62C5C8;
    }
    .video__from{
        margin-top:25rpx;
        font-size: 24rpx;
        margin-bottom:20rpx;
    }
    .from-tip{
        color: #BBBBBB;
    }
    .from-position{
        color: #FF5E5E;
        margin-left:25rpx;
    }
    .video-line{
        width:730rpx;
        height:2rpx;
        margin:0 auto;
        background: #DFDFDF;
    }
</style>