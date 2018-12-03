<template>
     <div class="heat-puretext">
         <postuser-head></postuser-head>
            <!-- <div class="puretext-body">
                <div class="title-wrap">
                    <div 
                    class="puretext-title"
                    :class="{showPart:isShow}"
                    >
                        宝宝两岁半，就喜欢吃糖，一出门就要买糖吃
                        一天吃好几根棒棒糖，怎么办宝宝两岁半，就
                        喜欢吃糖，一出门就要买糖吃一天吃好几根棒
                        棒糖，怎么办？怎么办？来自星星的问候,深圳市南山区高新园福安科技大厦,中华人民共和国万岁
                    </div>
                    <span class='read-all' @click="handleShowPart">{{showtext}}</span>
                </div>
            </div> -->
            <post-content></post-content>
            <vote-block :favorNum=1 :againstNum=2></vote-block>
            <comment-list></comment-list>
            <from-block></from-block>
            <location></location>
            <bottom-like></bottom-like>
        </div><!--热议卡片-->
</template>
<script>
import PostuserHead from '@/public-components/postuser-head'
import FromBlock from '@/public-components/from-block'
import VoteBlock from '@/public-components/vote-block'
import BottomLike from '@/public-components/bottom-like'
import CommentList from '@/public-components/comment-list'
import PostContent from '@/public-components/post-content'
import Location from '@/public-components/location'
    export default {
        components:{
           PostuserHead,
           FromBlock,
           VoteBlock,
           BottomLike,
           CommentList,
           PostContent,
           Location 
        },
        data() {
            return {
                isShow:true
            }
        },
        methods:{
            handleShowPart() {
                this.isShow = ! this.isShow
            }
        },
        computed:{
            showtext(){
                return  this.isShow?"查看全文":"收起"
            }
        }
    }
</script>
<style lang="css" scoped>
    .heat-puretext{
        width:730rpx;
        margin:0 auto;
        background: #FFFFFF;
        border-radius: 46.85rpx 10rpx 10rpx 10rpx;
        margin-bottom:20rpx;
    }
    .puretext__heading{
        display:flex;
        height:90rpx;
    }
    .heading-icon{
        width:90rpx;
        height:90rpx;
        margin-left:13rpx;
    }
    .heading-desc{
        flex:1;
        margin-left:20rpx;
        display:flex;
        flex-direction:column;
        justify-content:center;
    }
    .desc-username{
        font-size: 28rpx;
        color: #8E8E8E;
    }
    .desc-time{
        font-size: 20rpx;
        color: #BBBBBB;
    }
    .time{
        margin-right:10rpx;
    }
    .heading-nav{
        width:70rpx;
        display:flex;
        justify-content:center;
    }
    .nav-img{
        width:15rpx;
        height:29rpx;
        transform:rotate(90deg);
        margin-top:10rpx;
    }
    .puretext-body{
        margin-top:10rpx;
        width:690rpx;
        margin:0 auto;
    }
    .puretext-title{
        width:640rpx;
        font-size: 32rpx;
        color: #333333;
        /* display:inline-block; */
    }
    .showPart{
       display:-webkit-box;
       -webkit-box-orient:vertical;
       -webkit-line-clamp:4;
       overflow:hidden;
       text-overflow:ellipsis; 
    }
    .read-all{
        font-size: 32rpx;
        color: #677AA2;
    }
/**投票区域*/
 .heat__vote{
        margin-top:45rpx;
        height:64rpx;
        line-height:64rpx;
        display:flex;
        justify-content:space-between;
    }
    .vote-favor,.vote-against{
        display:flex;
        align-items:center;
    }
    .favor-img,.against-img{
        height:64rpx;
        width:64rpx;
        display:block;
    }
    .favor-status{}
    .favor-status-word{
        margin-left:20rpx;
        font-size: 24rpx;
        color: #FB5E62;
        line-height:33rpx;
    }
    .favor-status-bar{
        height:9rpx;
        width:200rpx;
        background: #FB5E62;
    }
    .against-status{}
    .against-status-word{
        margin-left:20rpx;
        font-size: 24rpx;
        color: #62C5C8;
        line-height:33rpx;
    }
    .against-status-bar{
        height:9rpx;
        width:384rpx;
        background:#62C5C8;
    }
/*热议回复区块*/
    
/**************************************/
    .puretext__vote{
        margin-top:40rpx;
        height:90rpx;
        border-top:2rpx solid #DFDFDF;
        display:flex;
        align-items:center;
    }
    .vote-line{
        width:4rpx;
        height:45rpx;
        background:#DFDFDF;
    }
    .vote-like,.vote-reply{
        flex:1;
        display:flex;
        justify-content:center;
        align-items:center;
        font-size: 28rpx;
        color: #8E8E8E;
    }
    .like-img,.reply-img{
        height:42rpx;
        width:40rpx;
        display:block;
    }
    .like-num,.reply-num{
        margin-left:20rpx;
    }
    /***来自哪个帖子*/
    .puretext__from{
        margin-top:25rpx;
        font-size: 24rpx;
        margin-bottom:20rpx;
    }
    .from-tip{
        color: #BBBBBB;
    }
    .from-position{
        color: #FF5E5E;
        margin-left:25rpx;
    }
</style>