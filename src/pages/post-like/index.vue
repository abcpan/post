<template>
    <div>
        <post-card></post-card>
        <no-comment></no-comment>
        <input-card></input-card>
        <comment-card></comment-card>
    </div>
</template>
<script>
import PostCard from './components/post-card'
import NoComment from './components/no-comment'
import InputCard from './components/input-card'
import CommentCard from './components/comment-card'
export default {
    components:{
        PostCard,
        NoComment,
        InputCard,
        CommentCard
    }
}
</script>
<style lang="css">
    
</style>