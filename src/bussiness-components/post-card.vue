<template>
     <div class="post">
         <PostlikeHead :userInfo="post.userInfo"></PostlikeHead>
         <post-content :postContent="post.postContent"></post-content>
         <imgBlock :imgInfo="post.imgInfo"></imgBlock>
         <from-block :postFrom="post.postFrom"></from-block>
         <Location :location="post.location"></Location> 
         <postlike-list :wholike="post.wholike"></postlike-list>
            <!--评论提示信息-->
        </div><!--帖子卡片-->
</template>
<script>
import PostlikeHead from  '@/public-components/postlike-head'
import FromBlock from  '@/public-components/from-block'
import Location from  '@/public-components/location'
import PostContent from  '@/public-components/post-content'
import imgBlock from  '@/public-components/img-block'
import PostlikeList from  '@/public-components/postlike-list'
    export default {
        components:{
            PostlikeHead,
            FromBlock,
            Location,
            PostContent,
            imgBlock,
            PostlikeList
        },
        data() {
            return {
                post:{
                    "userInfo":{"avatarUrl":"/static/user.png","username":"刁蛮公主","replyTime":68,"focus":true},
                    "postContent":"宝宝两岁半，就喜欢吃糖，一出门就要买糖吃好几根棒棒糖，怎么办？怎么办？怎……就要吃你烦不烦啊  真的很恼火,再闹把你丢给熊嘎婆",
                    "voteInfo":{"isVote":false,"favorNum":123456,"againstNum":1234},
                    "imgInfo":{
                        "imgUrls":[
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041314&di=15f898495007e788033a6484fe866097&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F015da9554971170000019ae9f43459.jpg%402o.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041314&di=7ca13babc86b8e6c30490eb24f10943f&imgtype=0&src=http%3A%2F%2Ftxt22262.book118.com%2F2017%2F0424%2Fbook100676%2F100675491.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041305&di=7d3f615477a9d1d0c4313ebc68bb193f&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F01fbe655dfe31932f875a1328a500b.jpg%40900w_1l_2o_100sh.jpg",
                        "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1543912041305&di=7d3f615477a9d1d0c4313ebc68bb193f&imgtype=0&src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F01fbe655dfe31932f875a1328a500b.jpg%40900w_1l_2o_100sh.jpg"
                        ],
                        "parrentWidth":700
                    },
                    "postFrom":"宝宝的问题在哪里",
                    "comment":{
                        "content":"宝宝到底要吃什么好,最近宝宝老是拉肚子,睡眠也不好我都不知道怎么办了",
                        "isHot":false,
                        "list":[
                            {"name":"娇兰佳人","replyContent":"我真的好想再活500年"},
                            {"name":"天线宝宝","replyContent":"泥煤,长得这么丑"},
                            {"name":"蟑螂恶霸","replyContent":"哼,我要和平星,我要干死卡布达"},
                            {"name":"蝎子来来","replyContent":"大哥,咱让喊上蜘蛛侦探在来和他么抢和平星"},
                            {"name":"牛顿","replyContent":"妈的,这苹果砸得我真疼"}
                        ]
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
                     ]
                }
            }
        }
    }
</script>
<style lang="css" scoped>
</style>