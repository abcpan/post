<template>
     <div class="post">
            <div class="post__heading">
                <img class="heading-icon" src="../../assets/images/icon.png" mode="aspectFill" alt="">
                <div class="heading-desc">
                    <div class="desc-username">匿名</div>
                    <div class="desc-time"><span class="time">刚刚</span>回复</div>
                </div>
                <div class="heading-nav"><img class="nav-img" src="../../assets/images/path.png" alt="" mode="aspectFill" ></div>
            </div>
            <div class="post-body">
                <div class="body-wrap">
                    <div class="post__content">
                           <div class="content-wrap">
                               宝宝两岁半，就喜欢吃糖，一出门就要买糖吃
                                一天吃好几根棒棒糖，怎么办宝宝两岁半，就
                                喜欢吃糖，一出门就要买糖吃一天吃好几根棒
                                棒糖，怎么办？怎么办？我么秒内阿胶方法in哦么恶疾诶恶疾ii
                           </div><!--此处待处理-->
                           <div class="content-reply">
                               <p>【支持】陪孩子和老公出去玩</p>
                               <p>【支持】陪孩子和老公出去玩</p>
                           </div>
                    </div><!--内容区域-->
                    <div class="post__vote">
                            <img  
                                class="favor-img" 
                                :src="favor" 
                                mode="aspectFill" alt=""
                                @click="doFavor"
                            />
                            <div class="vote-status">
                                <div class="word">
                                    <div class="favor-status-word" v-if="favorNum">{{favorNum}}人支持</div>
                                    <div v-else class="favor-status-word">支持</div>
                                    <div class="against-status-word" v-if="againstNum">{{againstNum}}人反对</div>
                                    <div v-else class="against-status-word">反对</div>
                                </div>
                                <div class="bar-block">
                                    <div class="favor-status-bar" :style="favorstyle"></div>
                                    <div class="against-status-bar" :style="againststyle"></div>
                                </div>
                            </div>
                            <img 
                                class="against-img" 
                                :src="against" 
                                mode="aspectFill"
                                @click="doAgainst"
                            />
                    </div><!--投票区域-->
                    <div class="post__from">
                        <span class="from-tip">来自</span>
                        <span class="from-position">宝宝的问题里问</span>
                    </div>
                </div>
            </div><!--帖子的身体-->
            <div class="post-line"></div>
        </div><!--帖子卡片-->
</template>
<script>
    export default {
        data() {
            return {
                favorNum:0,
                againstNum:0,
                favor:'../../assets/images/favor-default.png',
                against:'../../assets/images/favor-default.png'
            }
        },
        methods:{
            doFavor() {
                this.favorNum +=1
                this.favor = '../../assets/images/favor.png',
                this.against ='../../assets/images/against.png'
            },
            doAgainst() {
                this.againstNum += 1
            }
        },
        computed:{
            favorstyle() {
                let width = (this.favorNum/(this.favorNum+this.againstNum))*562
                return `width:${width}rpx`
            },
            againststyle(){
                let width = (this.againstNum/(this.favorNum+this.againstNum))*562
                return `width:${width}rpx`
            }
        },
        updated(){
            console.log(this.favorstyle)
        }
    }
</script>
<style lang="css" scoped>
    .post{
        padding-top:20rpx;
        background:#fff;
    }
    .post__heading{
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
    .post-body{
        margin-top:10rpx;
    }
    .body-wrap{
        width:690rpx;
        margin:0 auto;
    }
    .post__content{
        font-size: 32rpx;
        color: #333333; 
    }
    .content-wrap{
        width:640rpx;
        display:-webkit-box;
        -webkit-box-orient:vertical;
        -webkit-line-clamp:4;
        overflow:hidden;
        text-overflow:ellipsis;
    }
    .content-reply{
        margin:50rpx 0 0 10rpx;
    }
    .post__vote{
        margin-top:45rpx;
        height:64rpx;
        line-height:64rpx;
        display:flex;
        justify-content:space-between;
    }
    .favor-img,.against-img{
        height:64rpx;
        width:64rpx;
        display:block;
    }
    .vote-status{
        flex:1;
    }
    .word{
        display:flex;
        justify-content:space-between;
    }
    .bar-block{
        display:flex;
        justify-content:space-between;
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
        background: #FB5E62;
    }
    .against-status-word{
        margin-right:20rpx;
        font-size: 24rpx;
        color: #62C5C8;
        line-height:33rpx;
    }
    .against-status-bar{
        height:9rpx;
        background:#62C5C8;
    }
    /* .against-status-bar,.favor-status-bar{
        margin-bottom:30rpx;
    } */
    .post__from{
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
    .post-line{
        width:730rpx;
        height:2rpx;
        margin:0 auto;
        background: #DFDFDF;
    }
</style>