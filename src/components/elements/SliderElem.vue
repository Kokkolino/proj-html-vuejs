<template>
    <div id="container">
        <section id="imgSection" :class="[cover == true ? 'cover' : 'contain']" :style='{backgroundImage: "url("+require(`../../assets${slides[position]}`)}'>
        </section>
        <div id="dots">
            <span  v-for="(elem, index) in slides" :key="index">
                <div class="square active"  :style="{border: `2px solid ${color}`}" v-if="position==index"></div>
                <div class="square inactive" :style="{border: `2px solid ${color}`}" v-else v-on:click="position = index"></div>
            </span>
        </div>
    </div>
</template>

<script>

    export default {
        name: 'SliderElem',
        props: {
            slides: Array,
            color: String,
            cover: Boolean,
        },
        data(){
            return{
                position: 0
            }
        },
         mounted(){
             setInterval(this.swapPhoto, 3000);
         },
         methods: {
             swapPhoto: function(){
                 const max = this.slides.length - 1;
                 if(this.position == max){
                 return this.position = 0;
                 }
                 return this.position++;
             }
         }

    }
</script>

<style lang="scss" scoped>
    #imgSection{
        height: 100%;
        background-repeat: no-repeat;
    }

    .cover{
        background-size: cover;
    }

    .contain{
        background-size: contain;
    }

    #container{
        width: 100%;
        height: 100%;
        position: relative;
    }

    #dots{
        position: absolute;
        bottom: 0;
        left: 29%;
    }
   
    .square{
        width: 20px;
        height: 8px;
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