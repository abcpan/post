<template>
    <div class="comment-list-wrap">
        <div class="comment-main">
            {{comment.content}}
        </div>
        <div class="comment-wrap" :class="[comment.isHot?'comment-wrap--heat':'']">
            <ul class="comment-list"
            >
                <li class="discuss-item" v-for="(item,index) in list" :key="index">
                    <span class="name">{{item.name}}:</span>{{item.replyContent}}
                </li>
            </ul>
            <span class="comment-tip" @click="handleLookMore" v-if="more">{{moretip}}</span>
        </div>
   </div>
</template>
<script>
    export default {
        props:{
            comment:Object
        },
        data() {
            return {
                list:this.comment.list.slice(0,this.comment.showCommentNum),
                more:this.comment.list.length >this.comment.showCommentNum, //判断是否大于评论对象中规定显示的评论数量 是的话就显示 '查看更多的评论'
                moretipchange:!this.comment.list.length >this.comment.showCommentNum  // 设置提示文字切换boolean 默认没有变更
            }
        },
        mounted() {},
        methods:{
            handleLookMore() {
                if(!this.moretipchange){  //判断文字是否改变
                    this.list = this.comment.list
                    this.moretipchange= true
                }else{
                    this.list= this.comment.list.slice(0,this.comment.showCommentNum)
                    this.moretipchange = false  // 切换回灭有提示有更多评论状态
                }  
            }
        },
        computed:{
            moretip(){
                if(!this.moretipchange) {
                    let replyNum = this.comment.list.length -this.comment.showCommentNum;
                    return `查看另外${replyNum}条评论`
                }else{
                    return "收起评论"
                }
            }
        }
    }
</script>
<style lang="scss" scoped>
    .comment-list-wrap{
        display:flex;
        flex-direction:column;
        justify-content:center;
        margin:0 40rpx;
    }
    .comment-main{
        font-size: 32rpx;
        color: #333333;
    }
    .comment-list{
      display:-webkit-box;
      -webkit-box-orient: vertical;
      -webkit-line-clamp:2;
      overflow: hidden;
    }
    .comment-wrap{
        margin-top:10rpx;
        background-color:#F6F6F6;
        padding:0 20rpx 0 20rpx;
        border-radius: 8rpx;
    }
    .comment-wrap--heat{
      padding-top:20rpx;
      background:#F6F6F6 url('../assets/images/heat-discuss-min.png') no-repeat left top;
      background-size:6%;
    }
    .discuss-item,.comment-tip{
        font-size:28rpx;
        color: #151515;
        line-height:40rpx;
    }
    .name,.comment-tip{
        color: #5C6F98;
        margin-right:10rpx;
    }
</style>