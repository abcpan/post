<template>
    <div class="post-pictures">
        <img  class="picture" v-for="(item,index) of selfPictures" :src="item" :key="index">
   </div>
</template>
<script>
    export default {
        props:{
            pictures:Array
        },
        data() {
            return {
                selfPictures:this.pictures.slice(0,3)
            }
        }
    }
</script>
<style lang="css" scoped>
    .post-pictures{
        margin:20rpx 0 0 20rpx;
        display:flex;
    }
    .picture{
        height:180rpx;
        width:180rpx;
        display:block;
        background:#8E8E8E;
        margin-right:16rpx;
    }
</style>
