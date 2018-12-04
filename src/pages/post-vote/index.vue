<template>
    <div>
        <div class="title">
            <div class="title__tip"><span>来自</span><span class="tip-name">投票区</span></div>
            <img class="title__icon" mode="aspectFill" src="../../assets/images/path.png" alt=""/>
        </div>
        <post-vote></post-vote>
        <comment-card></comment-card>
        <bottom-input></bottom-input>
    </div>
</template>
<script>
import PostVote from '@/bussiness-components/post-vote'
import BottomInput from '@/public-components/bottom-input'
import CommentCard from '@/bussiness-components/comment-card'
export default {
    components:{
        CommentCard,
        PostVote,
        BottomInput
    },
    data() {
        return {
            pathImg:'/static/path.png'
        }
    }
}
</script>
<style lang="css" scoped>
    .title{
        width:100%;
        height:60rpx;
        background: #F1F1F1;
        line-height:60rpx;
        font-size: 24rpx;
        color: #BBBBBB;
        display:flex;
        justify-content:space-between;
    }
    .tip-name{
        color:#FF5E5E;
        padding-left:20rpx;
    }
    .title__tip{
        margin-left:30rpx;
    }
    .title__icon{
        width:15rpx;
        height:26rpx;
        margin-right:30rpx;
        margin-top:20rpx;
    }
</style>