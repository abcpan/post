<template>
    <div class="user-heading">
        <img class="user-heading__icon" :src="userInfo.avatarUrl" mode="aspectFill" alt="">
        <div class="user-heading__desc">
            <div class="username">{{userInfo.username}}</div>
            <div class="usertime">
                <span class="usrtime--current">{{replyTime}}</span>
                回复
            </div>
        </div>
        <div class="user-heading__nav">
            <img 
                class="nav__img" 
                src="/static/path.png" 
                alt="" 
                mode="aspectFill" 
            >
        </div>
    </div>
</template>
<script>
    export default {
        props:{
            userInfo:Object
        },
        data(){},
        computed:{
            replyTime() {
                let replyTime = null
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
    .user-heading{
        display:flex;
        padding:20rpx 0 0 10rpx;
        &__icon{
            width:90rpx;
            height:90rpx;
        }
        &__desc{
            flex:1;
            margin-left:20rpx;
            display:flex;
            flex-direction:column;
            justify-content:center;
            .username{
                font-size: 28rpx;
                color: #8E8E8E;
            }
            .usertime{
               font-size: 20rpx;
               color: #BBBBBB;
               &--current{
                   margin-right:20rpx;
               }
            }
        }
        &__nav{
            width:70rpx;
            display:flex;
            justify-content:center;
            .nav__img{
                width:15rpx;
                height:29rpx;
                transform:rotate(90deg);
                margin-top:10rpx;
            }
        }
    }
</style>
