<template>
     <div class="comment-card">
         <commentuser-head></commentuser-head>
         <comment-list></comment-list>
    </div><!--评论卡片-->
</template>
<script>
import CommentuserHead from '@/public-components/commentuser-head'
import CommentList from '@/public-components/comment-list'
export default{
    components:{
        CommentuserHead,
        CommentList
    }
}
</script>

<style lang="scss" scoped>
.comment-card::after{
    content:"";
    display:block;
    margin-top:20rpx;
    border-bottom:2rpx solid #CDCCCC;
    margin-left:112rpx;
}
</style>