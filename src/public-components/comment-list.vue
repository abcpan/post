<template>
    <div class="comment-list-wrap">
        <div class="comment-main">
            {{comment.content}}
        </div>
        <ul class="comment-list"
            :class="[comment.isHot?'comment-list--heat':'']"
        >
            <li class="discuss-item" v-for="(item,index) in list" :key="index">
                <span class="name">{{item.name}}:</span>{{item.replyContent}}
            </li>
        </ul>
   </div>
</template>
<script>
    export default {
        props:{
            comment:Object
        },
        data() {
            return {
                list:this.comment.list
            }
        },
        mounted() {
            console.log(this.comment)
        }
    }
</script>
<style lang="scss" scoped>
.comment-list-wrap{
        padding:0 40rpx;
        overflow:hidden;
    }
    .comment-main{
        font-size: 32rpx;
        color: #333333;
    }
    .comment-list{
      border-radius: 8rpx;
      padding:34rpx 52rpx 20rpx 30rpx;
      display:block;
    }
    .comment-list--heat{
      background:#F6F6F6 url('../assets/images/heat-discuss-min.png') no-repeat left top;
      background-size:6%;
    }
    .discuss-item{
        background-color:#F6F6F6;
        font-size:28rpx;
        color: #151515;
        line-height:40rpx;
    }
    .name{
        color: #5C6F98;
        margin-right:10rpx;
    }
</style>