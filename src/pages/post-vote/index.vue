<template>
    <div>
        <div class="title">
            <div class="title__tip"><span>来自</span><span class="tip-name">投票区</span></div>
            <img class="title__icon" mode="aspectFill" src="../../assets/images/path.png" alt=""/>
        </div>
        <post-vote></post-vote>
        <vote-result></vote-result>
        <comment-card></comment-card>
        <comment-card></comment-card>
        <input-card></input-card>
    </div>
</template>
<script>
import VoteResult from './components/vote-result'
import CommentCard from './components/comment-card'
import PostVote from '@/public-components/post-vote/post-vote'
import InputCard from './components/input-card'
export default {
    components:{
        VoteResult,
        CommentCard,
        PostVote,
        InputCard,
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