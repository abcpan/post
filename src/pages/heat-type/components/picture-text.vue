<template>
     <div class="post">
            <div class="post__heading">
                <img class="heading-icon" src="../../../assets/images/icon.png" mode="aspectFill" alt="">
                <div class="heading-desc">
                    <div class="desc-username">金木小公主</div>
                    <div class="desc-time"><span class="time">刚刚</span>回复</div>
                </div>
                <!-- <div class="heading-focus">
                    <div class="focus-button">
                        关注
                    </div>
                </div>       按钮区域 -->
            </div>
            <div class="post-body">
                <div class="body-wrap">
                    <div class="post__content">
                           <div class="content-wrap">
                               宝宝两岁半，就喜欢吃糖，一出门就要买糖吃
                                一天吃好几根棒棒糖，怎么办？
                           </div><!--此处待处理-->
                           <div class="content-pictures">
                               <img  class="picture" src="" alt="">
                               <img  class="picture" src="" alt="">
                               <img  class="picture" src="" alt="">
                           </div>
                    </div><!--内容区域-->
                    <div class="post__from">
                        <span class="from-tip">来自</span>
                        <span class="from-position">宝宝的问题里问</span>
                    </div>
                    <div class="address">
                        <img class="address-icon" src="../../../assets/images/position.png" mode="aspectFill" alt="">
                        <span class="address-tip">深圳市南山区科技园</span>
                        <span class="address-distance">一公里以内</span>
                    </div>
                </div>
            </div><!--帖子的身体-->
            <!-- <div class="post-line"></div> -->
            <!-- <div class="post-like">                  
                <div class="like-wrap">
                    <img  class="like-icon" src="../../../assets/images/like-default.png" mode="aspectFill" alt="">
                    <img  class="user-icon" src="" alt="">
                    <img  class="user-icon" src="" alt="">
                    <img  class="user-icon" src="" alt="">
                </div>
            </div> -->
            <!-- <div class="post-line"></div>            间隔线 -->
            <!--评论提示信息-->
            <!-- <div class="comment-info">
                <div class="info-tip">最新评论<span class="comment-num">6</span></div>
                <div class="info-sort">
                    从旧到新
                    <div class="arrow">
                        <div class="triangle"></div>
                        <div class="rect"></div>
                    </div>
                </div>
            </div> -->
            <div class="puretext__vote">
                <div class="vote-like">
                    <img  class="like-img" src="../../../assets/images/heart.png"  alt="">
                    <div class="like-num">123456</div>
                </div><!--投票区域-喜欢区域-->
                <div class="vote-line"></div>
                <div class="vote-reply">
                    <img class="reply-img" src="../../../assets/images/comment-icon.png"   alt=""/>
                    <div class="reply-num">123456</div>
                </div><!--投票区域-回复区域-->
            </div><!--回复区域-->
        </div><!--帖子卡片-->
</template>
<script>
    
</script>
<style lang="css">
    .post{
        padding-top:20rpx;
        background:#fff;
    }
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
    .post-body{
        margin-top:10rpx;
    }
    .body-wrap{
        width:690rpx;
        margin:0 auto;
    }
    .post__content{
        font-size: 32rpx;
        color: #333333; 
    }
    .content-wrap{
        width:640rpx;
        display:-webkit-box;
        -webkit-box-orient:vertical;
        -webkit-line-clamp:2;
        overflow:hidden;
        text-overflow:ellipsis;
    }
    .content-pictures{
        margin:20rpx 0 0 0;
        display:flex;
    }
    .picture{
        height:180rpx;
        width:180rpx;
        display:block;
        background:#8E8E8E;
        margin-right:16rpx;
    }
    .post__from{
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
    .post-line{
        width:730rpx;
        height:2rpx;
        margin:0 auto;
        background: #DFDFDF;
    }
    .address{
        font-size: 24rpx;
        color: #BBBBBB;
    }
    .address-icon{
        width:20rpx;
        height:28rpx;
        margin-right:48rpx;

    }
    .address-tip{
        margin-right:30rpx;
    }
    .like-wrap{
        width:730rpx;
        margin:0 auto;
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
    .puretext__vote{
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
</style>