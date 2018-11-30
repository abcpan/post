<template>
    <div>
        <heat-vote></heat-vote>
        <vote-result></vote-result>
    </div>
</template>
<script>
import HeatVote from './components/heat-vote'
import VoteResult from './components/vote-result'
    export default {
        components:{
            HeatVote,
            VoteResult
        }
    }
</script>
<style lang="css">
page{
    background:#eee;
}
</style>