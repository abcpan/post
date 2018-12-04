 <template>
<div class="comment-head">
    <img class="comment-head__icon" :src="userInfo.avatarUrl" mode="aspectFill" alt="">
    <div class="comment-head__desc">
        <div class="username">{{userInfo.username}}</div>
        <div class="time">{{replyTime}}</div>
    </div>
    <div class="comment-head__function">
        <div class="function__favor">
            {{likeNum}}
            <img 
                class="favor-img" 
                :src="sweetUrl" 
                mode="aspectFill"
                @click="handleFavor"
            >
        </div>
        <div class="function__reply">
            {{replyNum}}
            <img class="reply-img"
            src="/static/reply-icon.png" 
            mode="aspectFill" >
        </div>
    </div>
</div>
 </template>
 <script>
     export default {
         props:{
             userInfo:Object,
             likeandreply:Object
         },
         data() {
             return {
                 likeNum:this.likeandreply.likeNum,
                 replyNum:this.likeandreply.replyNum,
                 sweetUrl:"/static/sweet-default.png",
                 isLike:this.likeandreply.isLike
             }
         },
         methods:{
             handleFavor() {
                 if(!this.isLike){
                    this.sweetUrl = "/static/sweet.png"
                    this.likeNum+=1
                    this.isLike = true
                 }
             }
         },
         computed:{
             replyTime() {
                let time = this.userInfo.replyTime/60
                let hours = Math.floor(time)
                let mimutes = parseInt((time-hours)*60)
                console.log(mimutes)
                if(hours && mimutes) {
                    return hours +'小时' + mimutes+ '分钟' + '前'
                }else if(hours && !mimutes) {
                    return hours +'小时'+ '前'
                }else if(!hours && mimutes){
                    return mimutes+ '分钟' + '前'
                }else{
                    return "刚刚"
                }
            }
         }
     }
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
                    margin-left:10rpx;
                }
            }
            .function__reply{
                display:flex;
                align-items:center;
                margin-left:20rpx;
                .reply-img{
                    width:40rpx;
                    height:31rpx;
                    padding:10rpx;
                    margin-left:10rpx;
                }
            }
        }
    }
 </style>
 
 