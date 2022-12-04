<template>
    <div id="container">
        <section id="imgSection">
            <img :src="require(`../../assets${slides[position]}`) ">
        </section>
        <div id="dots">
            <span  v-for="(elem, index) in slides" :key="index">
                <div class="square active" v-if="position==index"></div>
                <div class="square inactive" v-else v-on:click="position = index"></div>
            </span>
        </div>
    </div>
</template>

<script>

    export default {
        name: 'SliderElem',
        props: {
            slides: Array
        },
        data(){
            return{
                position: 0
            }
        },
        // mounted(){
        //     setInterval(this.swapPhoto, 2000);
        // },
        // methods: {
        //     swapPhoto: function(){
        //         const max = this.imgObj.length - 1;
        //         if(this.index == max){
        //         return this.index = 0;
        //         }
        //         return this.index++;
        //     }
        // }

    }
</script>

<style lang="scss" scoped>
    #container{
        width: 100%;
        position: relative;;
    }

    #dots{
        position: absolute;
        bottom: 0;
        left: 29%;
    }
   
    .square{
        width: 20px;
        height: 8px;
        border: 2px solid #fe6601;
        margin: 10px;
        display: inline-block;
    }

    img{
        width: 100%;
    }

    .active{
        position: relative;
        bottom: 6px;
    }
</style>