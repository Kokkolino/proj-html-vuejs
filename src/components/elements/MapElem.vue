<template>
    <div>
        <div class="mapouter">
            <div class="gmap_canvas">
                <iframe width="100%" height="100%" id="gmap_canvas" src="https://maps.google.com/maps?q=45%C2%B023'45.6%22N75%C2%B040'35.6%22W&t=&z=13&ie=UTF8&iwloc=&output=embed" frameborder="0" scrolling="no" marginheight="0" marginwidth="0">
                </iframe>
            
        </div></div>
    </div>
</template>

<script>
    export default {
        name: 'MapElem'
    }
</script>

<style lang="scss" scoped>
    .mapouter{
        position:relative;
        text-align:right;
        height:380px;
        width:100%;
    }
    .gmap_canvas {
        overflow:hidden;
        background:none!important;
        height:380px;
        width:100%;
        }
</style>