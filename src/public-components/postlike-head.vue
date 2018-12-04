<template>
<div class="post__heading">
    <img class="heading-icon" :src="avatarUrl" mode="aspectFill" alt="">
    <div class="heading-desc">
        <div class="desc-username">{{userInfo.username}}</div>
        <div class="desc-time"><span class="time">{{replyTime}}</span>回复</div>
    </div>
    <div class="heading-focus">
        <div class="focus-button"
             :class="{active:isFocus}"
             @click="handleFocus"
        >
            {{buttonText}}  
        </div>
    </div><!--按钮区域-->
</div>
</template>
<script>
    export default {
        props:{
            userInfo:Object
        },
        data(){
            return {
                avatarUrl:"/static/user.png",
                isFocus:this.userInfo.focus
            }
        },
        mounted() {
            this.avatarUrl = this.userInfo.avatarUrl
        },
        methods:{
            handleFocus(){
                this.isFocus = !this.isFocus
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
            },
            buttonText(){
                return this.isFocus?"取消关注":"+ 关注"
            }
         }
    }
</script>
<style lang="css" scoped>
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
    .active{
        background:#BBBBBB;
        color:#8E8E8E;
    }
</style>
