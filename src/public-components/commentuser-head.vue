 <template>
<div class="comment-head">
    <img class="comment-head__icon" src="/static/user.png" mode="aspectFill" alt="">
    <div class="comment-head__desc">
        <div class="username">妹妹小公主</div>
        <div class="time">30分钟前
            <span class="currenttime">前</span>
        </div>
    </div>
    <div class="comment-head__function">
        <div class="function__favor">
            21
            <img class="favor-img" src="/static/sweet-default.png" alt="" mode="aspectFill" >
        </div>
        <div class="function__reply">
            33
            <img class="reply-img" src="/static/reply-icon.png" alt="" mode="aspectFill" >
        </div>
    </div>
</div>
 </template>
 <script>
     
 </script>
 <style lang="scss" scoped>
    @mixin imgSize($width,$height) {
        height:$height;
        width:$width;
        display:block;
    }
     .comment-head{
        display:flex;
        padding:20rpx 20rpx 20rpx 30rpx;
        &__icon{
            @include imgSize(62rpx,62rpx)
        }
        &__desc{
            flex:1;
            margin-left:20rpx;
            display:flex;
            flex-direction:column;
            .username{
                font-size: 28rpx;
                color: #8E8E8E;
            }
            .time{
                font-size: 20rpx;
                color: #BBBBBB;
                .currenttime{
                    margin-left:10rpx;
                }
            }
        }
        &__function{
            min-width:160rpx;
            display:flex;
            justify-content:space-between;
            font-size:20rpx;
            color: #BBBBBB;
            .function__favor{
                display:flex;
                align-items:center;
                .favor-img{
                     width:40rpx;
                    height:34rpx;
                }
            }
            .function__reply{
                display:flex;
                align-items:center;
                .reply-img{
                    width:40rpx;
                    height:31rpx;
                    padding:10rpx;
                }
            }
        }
    }
 </style>
 
 