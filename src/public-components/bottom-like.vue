<template>
<div class="bottom__like">
    <div class="like">
        <img  
            class="like-img" 
            :src="likeImgUrl"
            @click="handleLike"
        />
        <span
            v-if="isShow"
            :class="[isShow?'animation':'']"
        >+1</span>
        <div class="like-num">{{likeNum}}</div>
    </div><!--投票区域-喜欢区域-->
    <div class="line"></div>
    <div class="reply">
        <img 
            class="reply-img" 
            src="/static/reply-icon.png"
            @click="handleReply"
        />
        <div class="reply-num">{{replyNum}}</div>
    </div><!--投票区域-回复区域-->
</div>
</template>
<script>
   export default {
       props:{

       },
       data() {
           return {
               likeNum:123456,
               replyNum:123456,
               likeImgUrl:"/static/heart-default.png",
               enable:true,
               isShow:false
           }
       },
       methods:{
           handleLike() {
               if(this.enable){
                   this.likeImgUrl = "/static/heart.png"
                   this.likeNum+=1
                   this.enable = false
                   this.isShow = true
                   setTimeout(()=>{
                        this.isShow = false
                   },600)
               }
           }
       }
   } 
</script>
<style lang="css">
@keyframes ani{
    0%{opacity:0.1;font-size:20rpx;}
    25%{opacity:0.3;font-size:25rpx;}
    50%{opacity:0.5;font-size:30rpx;}
    75%{opacity:0.8;font-size:35rpx;}
    100%{opacity:1;font-size:40rpx;}
}
.animation{
    display:inline-block;
    color:red;
    animation:ani 0.6s;
}
    .bottom__like{
        height:90rpx;
        border-top:2rpx solid #DFDFDF;
        display:flex;
        align-items:center;
    }
    .line{
        width:4rpx;
        height:45rpx;
        background:#DFDFDF;
    }
    .like,.reply{
        flex:1;
        display:flex;
        justify-content:center;
        align-items:center;
        font-size: 28rpx;
        color: #8E8E8E;
    }
    .like-img,.reply-img{
        height:42rpx;
        width:42rpx;
        display:block;
    }
    .like-num,.reply-num{
        margin-left:20rpx;
    }
</style>
