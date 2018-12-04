<template>
     <div class="from">
        <span class="from__tip">来自</span>
        <span class="from__position">{{postFrom}}</span>
    </div>
</template>
<script>
    
</script>
<script>
    export default {
        props:{
            postFrom:String
        }
    }
</script>
<style lang="scss" scoped>
    .from{
        font-size:24rpx;
       padding:25rpx 30rpx;
        &__tip{
            color: #BBBBBB;
        }
        &__position{
            color: #FF5E5E;
            margin-left:25rpx;
        }
    }
</style>