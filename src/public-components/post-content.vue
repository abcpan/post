<template>
<div class="content">
    <div class="content__wrap"
        :class="[type?'showPart':'']"
    >
        宝宝两岁半，就喜欢吃糖，一出门就要买糖吃
        一天吃好几根棒棒糖，怎么办宝宝两岁半，就
        喜欢吃糖，一出门就要买糖吃一天吃好几根棒
        棒糖，怎么办？怎么办？我么秒内阿胶方法in哦么恶疾诶恶疾ii
    </div><!--此处待处理-->
    <span class='read-all' @click="handleShowPart">{{showtext}}</span>
</div>
</template>
<script>
    export default {
        data() {
            return {
                type:true
            }
        },
        methods:{
            handleShowPart() {
                this.type = ! this.type
            }
        },
        computed:{
            showtext(){
                return  this.type?"查看全文":"收起"
            }
        }
    }
</script>
<style lang="scss" scoped>
    .content{
        font-size: 32rpx;
        color: #333333;
        padding:10rpx 20rpx 0 30rpx;
        &__wrap{
            padding:0 60rpx 0 0;
            width:640rpx;
        }
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
</style>