<template>
     <div class="comment">
            <div class="comment__heading">
                <img class="heading-icon" src="../../../assets/images/icon.png" mode="aspectFill" alt="">
                <div class="heading-desc">
                    <div class="desc-username">妹妹小公主</div>
                    <div class="desc-time"><span class="time">30分钟</span>前</div>
                </div>
                <div class="heading-function">
                    <div class="function-favor">21<img class="favor-img" src="../../../assets/images/favor-icon.png" alt="" mode="aspectFill" ></div>
                    <div class="function-discuss">33<img class="discuss-img" src="../../../assets/images/comment-icon.png" alt="" mode="aspectFill" ></div>
                </div>
            </div>
            <div class="comment__body">
               <div class="body-wrap">
                   <div class="comment-main">
                       是不是，我刚买了几个回来煮很不错哦味道我喜欢
                   </div>
                   <div class="re-comment">
                       <div class="re-item">
                           <span class="name">俏丽家人:</span>
                           最好打一顿，如果一顿不行，那就两顿。
                       </div>
                   </div>
               </div>
            </div><!--评论主体-->
            <div class="comment__line"></div>
        </div><!--评论卡片-->
</template>
<script>

</script>
<style lang="css" scoped>
    .comment{
        padding-top:20rpx;
        background:#fff;
    }
    .comment__heading{
        display:flex;
        height:62rpx;
        margin-bottom:18rpx;
    }
    .heading-icon{
        width:62rpx;
        height:62rpx;
        margin-left:30rpx;
    }
    .heading-desc{
        flex:1;
        margin-left:20rpx;
        display:flex;
        flex-direction:column;
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
    .heading-function{
        display:flex;
        justify-content:space-between;
        font-size:20rpx;
        color: #BBBBBB;
        margin-right:30rpx;
    }
    .function-discuss,{
       
    }
    .function-favor{
        margin-right:40rpx;
    }
    .favor-img,.discuss-img{
        display:inline-block;
    }
    .favor-img{
        width:40rpx;
        height:34rpx;
        padding:10rpx;
    }
    .discuss-img{
        width:40rpx;
        height:31rpx;
        padding:10rpx;
    }

/*评论身体*/
.body-wrap{
    width:545rpx;
    margin:0 auto
}
.comment-main{
   font-size: 32rpx;
    color: #333333;
    line-height: 45rpx; 
}
.re-comment{
    margin-top:10rpx;
    background: #F6F6F6;
    border-radius: 8rpx;
}
.re-item{
    font-size:28rpx;
    color: #151515;
    line-height:40rpx;
}
.name{
    color: #5C6F98;
}
.comment__line{
    margin-top:30rpx;
    width:638rpx;
    height:2rpx;
    background:#CDCCCC;
    margin-left:112rpx;
}
</style>