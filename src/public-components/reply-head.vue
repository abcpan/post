<template>
    <div class="reply-head">
        <div class="reply__owner">
            <div class="owner-wrap">
                <span>回复:</span>
                <span class="owner-name">{{replyWho}}</span>
            </div>
        </div>
        <div class="reply__time">
            <div class="time-wrap">
                <img  class="time__clock" src="/static/clock.png" alt="">
                <span class="time__tip">{{replyTime}}回复</span>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    props:{
        replyWho:String,
        replyTime:Number
    },
    data() {
        return{}
    },
    onShow() {
        console.log(this.replyWho,this.replyTime)
    }
}
</script>
<style lang="css" scoped>
    .reply-head{
        height:80rpx;
        background:#eee;
        display:flex;
        align-items:center;
        justify-content:space-between;
        color: #8E8E8E;
    }
    .reply__owner{
        font-size:28rpx;
        display:flex;
    }
    .owner-name{
        color: #00003E;
        margin-left:20rpx;
    }
    .reply__time{
        height:64rpx;
        font-size: 20rpx;
        display:flex;
        align-items:flex-end;
    }
    .time-wrap{

    }
    .time__clock{
        height:20rpx;
        width:20rpx;
    }
    .time__tip{
        margin-left:10rpx;
    }
</style>