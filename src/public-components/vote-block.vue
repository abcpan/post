<template>
    <div class="vote">
        <img  
            class="vote__img--favor" 
            :src="favor" 
            mode="aspectFill" alt=""
            @click="doFavor"
        />
        <div class="vote__status">
            <div class="status__word">
                <div class="status__word--favor" v-if="favorNum">{{favorNum}}人支持</div>
                <div v-else class="status__word--favor">支持</div>
                <div class="status__word--against" v-if="againstNum">{{againstNum}}人反对</div>
                <div v-else class="status__word--against">反对</div>
            </div>
            <div class="status__bar">
                <div class="status__bar--favor" :style="favorstyle"></div>
                <div class="status__bar--against" :style="againststyle"></div>
            </div>
        </div>
        <img 
            class="vote__img--against" 
            :src="against" 
            mode="aspectFill"
            @click="doAgainst"
        />
    </div>
</template>
<script>
    export default {
        props:{
            favorNum:Number,
            againstNum:Number
        },
       data() {
            return {
                favor:"/static/post-vote/favor-default.png",
                against:"/static/post-vote/against-default.png"
            }
        },
        methods:{
            doFavor() {
                this.favorNum +=1
                this.favor = '/static/post-vote/favor.png',
                this.against ='/static/post-vote/against.png'
                console.log(this.favorNum)
            },
            doAgainst() {
                this.againstNum += 1
            }
        },
        computed:{
            favorstyle() {
                let  width = (this.favorNum/(this.favorNum+this.againstNum))*100
                return `width:${width}%`
            },
            againststyle(){
                let width = (this.againstNum/(this.favorNum+this.againstNum))*100
                return `width:${width}%`
            }
        }
    }
</script>
<style lang="scss" scoped>
 %between{
    display:flex;
    justify-content:space-between;
}
    .vote{
        @extend %between;
        padding:20rpx 30rpx 20rpx 30rpx;
    &__img--favor,&__img--against{
        display:block;
        height:64rpx;
        width:64rpx;
    }
    &__status{
        flex:1;
        .status__word{
            @extend %between;
            font-size: 24rpx;
            line-height:33rpx;
            &--favor{
                margin-left:20rpx;
                color: #FB5E62;
            }
            .status__word--against{
                margin-right:20rpx;
                color: #62C5C8;
            }
        }
        .status__bar{
            @extend %between;
            height:9rpx;
            &--favor{
            background: #FB5E62;
            }
            &--against{
                background:#62C5C8;
            }
        }
    }

    }
</style>