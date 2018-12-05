<template>
    <div class="my-reply">
        <reply-card></reply-card>
        <reply-card></reply-card>
    </div>
</template>
<script>
import replyCard from '@/bussiness-components/reply-card'
export default {
    components:{
        replyCard
    }
}
</script>
<style lang="css">
page{
    background:#eee;
}
</style>