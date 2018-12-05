<template>
     <div class="heat-puretext">
        <postuser-head :userInfo="post.userInfo"></postuser-head>
        <post-content  :postContent="post.postContent"></post-content>
        <vote-block    :voteInfo="post.voteInfo" ></vote-block>
        <comment-list :comment="post.comment"></comment-list>
        <from-block :postFrom="post.postFrom"></from-block>
        <location :location="post.location"></location>
        <bottom-like :bottomLike="post.bottomLike"></bottom-like>
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
                isShow:true,
                 post:{
                    "userInfo":{"avatarUrl":"/static/user.png","username":"刁蛮公主","replyTime":68,"focus":true},
                    "postContent":"宝宝两岁半，就喜欢吃糖，一出门就要买糖吃好几根棒棒糖，怎么办？怎么办？怎……就要吃你烦不烦啊  真的很恼火,再闹把你丢给熊嘎婆",
                    "voteInfo":{"isVote":false,"favorNum":123456,"againstNum":1234},
                    "pictures":[
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041314&di=15f898495007e788033a6484fe866097&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F015da9554971170000019ae9f43459.jpg%402o.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041314&di=7ca13babc86b8e6c30490eb24f10943f&imgtype=0&src=http%3A%2F%2Ftxt22262.book118.com%2F2017%2F0424%2Fbook100676%2F100675491.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041305&di=7d3f615477a9d1d0c4313ebc68bb193f&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F01fbe655dfe31932f875a1328a500b.jpg%40900w_1l_2o_100sh.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041305&di=7d3f615477a9d1d0c4313ebc68bb193f&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F01fbe655dfe31932f875a1328a500b.jpg%40900w_1l_2o_100sh.jpg",
                     ],
                    "postFrom":"宝宝的问题在哪里",
                    "comment":{
                        "content":"宝宝到底要吃什么好,最近宝宝老是拉肚子,睡眠也不好我都不知道怎么办了",
                        "isHot":true,
                        "list":[
                            {"name":"娇兰佳人","replyContent":"我真的好想再活500年"},
                            {"name":"天线宝宝","replyContent":"泥煤,长得这么丑"},
                            {"name":"蟑螂恶霸","replyContent":"哼,我要和平星,我要干死卡布达"},
                            {"name":"蝎子来来","replyContent":"大哥,咱让喊上蜘蛛侦探在来和他么抢和平星"},
                            {"name":"牛顿","replyContent":"妈的,这苹果砸得我真疼"}
                        ],
                        "showCommentNum":2
                    },
                    "location":{"coordinate":"西天雷音寺","distance":"1.2"},
                    "wholike":[
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041314&di=15f898495007e788033a6484fe866097&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F015da9554971170000019ae9f43459.jpg%402o.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041314&di=7ca13babc86b8e6c30490eb24f10943f&imgtype=0&src=http%3A%2F%2Ftxt22262.book118.com%2F2017%2F0424%2Fbook100676%2F100675491.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041305&di=7d3f615477a9d1d0c4313ebc68bb193f&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F01fbe655dfe31932f875a1328a500b.jpg%40900w_1l_2o_100sh.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041305&di=7d3f615477a9d1d0c4313ebc68bb193f&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F01fbe655dfe31932f875a1328a500b.jpg%40900w_1l_2o_100sh.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041305&di=7d3f615477a9d1d0c4313ebc68bb193f&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F01fbe655dfe31932f875a1328a500b.jpg%40900w_1l_2o_100sh.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041305&di=7d3f615477a9d1d0c4313ebc68bb193f&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F01fbe655dfe31932f875a1328a500b.jpg%40900w_1l_2o_100sh.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041305&di=7d3f615477a9d1d0c4313ebc68bb193f&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F01fbe655dfe31932f875a1328a500b.jpg%40900w_1l_2o_100sh.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041305&di=7d3f615477a9d1d0c4313ebc68bb193f&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F01fbe655dfe31932f875a1328a500b.jpg%40900w_1l_2o_100sh.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041305&di=7d3f615477a9d1d0c4313ebc68bb193f&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F01fbe655dfe31932f875a1328a500b.jpg%40900w_1l_2o_100sh.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041305&di=7d3f615477a9d1d0c4313ebc68bb193f&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F01fbe655dfe31932f875a1328a500b.jpg%40900w_1l_2o_100sh.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041305&di=7d3f615477a9d1d0c4313ebc68bb193f&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F01fbe655dfe31932f875a1328a500b.jpg%40900w_1l_2o_100sh.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041305&di=7d3f615477a9d1d0c4313ebc68bb193f&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F01fbe655dfe31932f875a1328a500b.jpg%40900w_1l_2o_100sh.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041305&di=7d3f615477a9d1d0c4313ebc68bb193f&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F01fbe655dfe31932f875a1328a500b.jpg%40900w_1l_2o_100sh.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041305&di=7d3f615477a9d1d0c4313ebc68bb193f&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F01fbe655dfe31932f875a1328a500b.jpg%40900w_1l_2o_100sh.jpg",
                     ],
                     "bottomLike":{"islike":false,"likeNum":198,"replyNum":889}
                }
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