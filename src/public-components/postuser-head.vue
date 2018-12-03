<template>
    <div class="user-heading">
        <img class="user-heading__icon" src="/static/user.png" mode="aspectFill" alt="">
        <div class="user-heading__desc">
            <div class="username">匿名</div>
            <div class="usertime">
                <span class="usrtime--current">刚刚</span>
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
