<template>
     <div class="post">
         <PostlikeHead></PostlikeHead>
         <post-content></post-content>
         <PostPictures></PostPictures> 
         <from-block></from-block>
         <Location></Location> 
         <postlike-list></postlike-list>
            <!--评论提示信息-->
        </div><!--帖子卡片-->
</template>
<script>
import PostlikeHead from  '@/public-components/postlike-head'
import FromBlock from  '@/public-components/from-block'
import Location from  '@/public-components/location'
import PostContent from  '@/public-components/post-content'
import PostPictures from  '@/public-components/post-pictures'
import PostlikeList from  '@/public-components/postlike-list'
    export default {
        components:{
            PostlikeHead,
            FromBlock,
            Location,
            PostContent,
            PostPictures,
            PostlikeList
        }
    }
</script>
<style lang="css" scoped>
</style>