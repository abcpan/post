<template>
    <div class="comment-list-wrap">
        <ul class="comment-list"
            :class="[type?'comment-list--heat':'']"
        >
            <li class="discuss-item">
                <span class="name">俏丽家人:</span>最好打一顿.
            </li>
            <li class="discuss-item">
                <span class="name">俏丽家人:</span>最好打一顿.
            </li>
        </ul>
   </div>
</template>
<script>
    export default {
        props:{
            
        },
        data() {
            return {
                type:true
            }
        }
    }
</script>
<style lang="scss" scoped>
.comment-list-wrap{
        padding:0 40rpx;
        overflow:hidden;
    }
    .comment-list{
      border-radius: 8rpx;
      padding:34rpx 52rpx 20rpx 30rpx;
      display:block;
    }
    .comment-list--heat{
      background: #ccc url('../assets/images/heat-discuss-min.png') no-repeat left top;
      background-size:6%;
    }
    .discuss-item{
        font-size:28rpx;
        color: #151515;
        line-height:40rpx;
    }
    .name{
        color: #5C6F98;
    }
</style>