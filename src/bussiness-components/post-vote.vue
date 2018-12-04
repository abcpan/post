<template>
    <div class="post-vote">
        <postuser-head  :userInfo="post.userInfo"></postuser-head>
        <post-body  :postContent="post.postContent"></post-body>
        <vote-block :voteInfo="post.voteInfo"></vote-block>
        <from-block :postFrom="post.postFrom"></from-block>
    </div><!--帖子卡片-->
</template>
<script>
import VoteBlock from '@/public-components/vote-block'
import PostuserHead from '@/public-components/postuser-head'
import FromBlock from '@/public-components/from-block'
import PostBody from  '@/public-components/post-body'
    export default {
        components:{
            VoteBlock,
            PostuserHead,
            FromBlock,
            PostBody 
        },
        props:{

        },
        data() {
            return{
                post:{
                    "userInfo":{"avatarUrl":"/static/user.png","username":"匿名","replyTime":68},
                    "postContent":"宝宝两岁半，就喜欢吃糖，一出门就要买糖吃好几根棒棒糖，怎么办？怎么办？怎……就要吃你烦不烦啊  真的很恼火,再闹把你丢给熊嘎婆",
                    "voteInfo":{"isVote":false,"favorNum":123456,"againstNum":1234},
                    "postFrom":"宝宝的问题在哪里"
                }
            }
        },
        mounted() {
        }
    }
</script>
<style lang="scss" scoped>
 %between{
    display:flex;
    justify-content:space-between;
}
    .post-vote{
        background:#fff;
        &::after{
            content:"";
            display:block;
            width:730rpx;
            border-top:2rpx solid #ccc;
            margin:20rpx 0 10rpx 10rpx;
        }
        &:last-child{
            &::after{
                display:none;
            }
        }
        &__cell{
        }
    }
</style>