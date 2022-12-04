<template>
    <li @mouseover="onPosition" @mouseout="outPosition">
        <div class="sprites"
         :style='{background: "url("+require(`../../assets/${NavData.img}`) +`)0 ${hoverPosition}`,}'></div>
        <span>
            {{NavData.title}}
        </span>
    </li>   
</template>

<script>
    export default {
        name: 'NavElem',
        props: {
            NavData: Object,
        },
        data(){
            return{
                hoverPosition: 0,
            }
        },
        methods: {
            onPosition: function(){
                this.hoverPosition = "32px"
            },
            outPosition: function(){
                this.hoverPosition = "0"
            }
        }
    }
</script>

<style lang="scss" scoped>
   
    li:hover{
        background-color: #fe6601;
        cursor: pointer;
    }
  
</style>