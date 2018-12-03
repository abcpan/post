<template>
    <div class="post-vote">
        <postuser-head></postuser-head>
        <post-body></post-body>
        <vote-block :favorNum=0 :againstNum=0></vote-block>
        <from-block></from-block>
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
        position:relative;
        &::after{
            content:"";
            display:block;
            width:730rpx;
            border-top:2rpx solid #ccc;
            position:absolute;
            bottom:0;
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