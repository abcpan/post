<template>
     <div class="heat-puretext">
            <div class="puretext__heading">
                <img class="heading-icon" src="../../../assets/images/icon.png" mode="aspectFill" alt="">
                <div class="heading-desc">
                    <div class="desc-username">匿名</div>
                    <div class="desc-time"><span class="time">刚刚</span>回复</div>
                </div>
                <div class="heading-nav"><img class="nav-img" src="../../../assets/images/path.png" alt="" mode="aspectFill" ></div>
            </div>
            <div class="puretext-body">
                <div class="puretext-title">
                    宝宝两岁半，就喜欢吃糖，一出门就要买糖吃
                    一天吃好几根棒棒糖，怎么办宝宝两岁半，就
                    喜欢吃糖，一出门就要买糖吃一天吃好几根棒
                    棒糖，怎么办？怎么办？我么秒内阿胶方法in哦么恶疾诶恶疾ii
                </div><!--此处待处理-->
                <div class="discuss">
                  <div class="discuss-wrap">
                      <div class="discuss-item">
                          <span class="name">俏丽家人:</span>
                          最好打一顿。
                      </div>
                      <div class="discuss-item">
                          <span class="name">俏丽家人:</span>
                          最好打一顿，如果一顿不行，那就两顿。
                      </div>
                      <div class="discuss-item">
                          <span class="name">俏丽家人:</span>
                          最好打一顿，如果一顿不行，那就两顿。
                      </div>
                      <div class="discuss-item">
                          <span class="name">俏丽家人:</span>
                          最好打一顿，如果一顿不行，那就两顿。
                      </div>
                      <div class="discuss-item">
                          <span class="name">俏丽家人:</span>
                          最好打一顿，如果一顿不行，那就两顿。
                      </div>
                      <div class="discuss-item">
                          <span class="name">俏丽家人:</span>
                          最好打一顿，如果一顿不行，那就两顿。哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈哈
                      </div>
                    </div>
                </div>
                <div class="post__from">
                    <span class="from-tip">来自</span>
                    <span class="from-position">宝宝的问题里问</span>
                </div><!--来自哪个帖子-->
            </div><!--热议身体-->
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
        </div><!--热议卡片-->
</template>
<script>
    export default {
        data() {
            return {
                puretextUrl:"http://wxsnsdy.tc.qq.com/105/20210/snsdypuretextdownload?filekey=30280201010421301f0201690402534804102ca905ce620b1241b726bc41dcff44e00204012882540400&bizid=1023&hy=SH&fileparam=302c020101042530230204136ffd93020457e3c4ff02024ef202031e8d7f02030f42400204045a320a0201000400"
            }
        }
    }
</script>
<style lang="css" scoped>
    .heat-puretext{
        width:730rpx;
        margin:0 auto;
        background: #FFFFFF;
        border-radius: 46.85rpx 10rpx 10rpx 10rpx;
        margin-bottom:20rpx;
    }
    .puretext__heading{
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
    .puretext-body{
        margin-top:10rpx;
        width:690rpx;
        margin:0 auto;
    }
    .puretext-title{
        width:640rpx;
        display:-webkit-box;
        -webkit-box-orient:vertical;
        -webkit-line-clamp:2;
        overflow:hidden;
        text-overflow:ellipsis;
        font-size: 32rpx;
        color: #333333;
    }
/*热议回复区块*/
    .discuss{
        width:670rpx;
        background: #F6F6F6;
        border-radius: 8rpx;
        margin:0 auto; 
        margin-top:30rpx;
        overflow:hidden;
        background:url('../../../assets/images/heat/heat-discuss.png') no-repeat left top;
        background-size:6%;
    }
    .discuss-wrap{
      width:588rpx;
      margin:34rpx 52rpx 20rpx 30rpx;
    }
    .discuss-item{
        font-size:28rpx;
        color: #151515;
        line-height:40rpx;
    }
    .name{
        color: #5C6F98;
    }
    /*来自哪里区域*/
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
/**************************************/
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
    /***来自哪个帖子*/
    .puretext__from{
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
</style>