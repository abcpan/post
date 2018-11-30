<template>
    <div class="heat-home">
        <heat-video></heat-video>
        <heat-puretext></heat-puretext>
        <picture-text></picture-text>
    </div>
</template>
<script>
import HeatVideo from './components/heat-video'
import HeatPuretext from './components/heat-puretext'
import PictureText from './components/picture-text'
    export default {
        components:{
            HeatVideo,
            HeatPuretext,
            PictureText
        }
    }
</script>
<style lang="css">
page{
    background:#eee;
}
</style>