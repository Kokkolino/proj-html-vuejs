<template>
    <div id="container">
        <section id="imgSection" style="background-size: cover; background-position: center;" :style='{backgroundImage: "url("+require(`../../assets${slides[position]}`)}'>
            <div id="alignCont">
                <div class="circles bordered">
                    <img src="../../assets/img/quote_alt.png" alt="">
                </div>
                <h1>
                    {{quotes[position].quote}}
                </h1>
                <div id="line">
                </div>
                <h3>
                    {{quotes[position].author}}
                </h3>
            </div>

            <div id="dots">
                <span  v-for="(elem, index) in slides" :key="index">
                    <div class="square active"  :style="{border: `2px solid ${color}`}" v-if="position==index"></div>
                    <div class="square inactive" :style="{border: `2px solid ${color}`}" v-else v-on:click="position = index"></div>
                </span>
            </div>

        </section>
    </div>
</template>

<script>
    export default {
        name: 'ParallaxElem',
        props: {
            slides: Array,
            color: String,
            quotes: Array
        },
        data(){
            return{
                position: 0
            }
        },
         mounted(){
            setInterval(this.swapPhoto, 5000);
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
    #container {
        width: 100%;
        height: 100%;
    }

    .circles{
        border-radius: 50%;
        height: 70px;
        width: 70px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .bordered{
       border: 2px solid white; 
    }
    h3{
        margin: 15px 0;
        color: white;
    }

    h1{
        color: white;
        width: 60%;
        font-size: 40px;
        font-weight: 100;
    }

    #imgSection{
        display: flex;
        flex-wrap: wrap;
        padding: 40px 0;
        height: 100%;
        position: relative;
    }

    #alignCont{
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 200px;
        gap: 20px;
        vertical-align: middle;
        flex-direction: column;
    }

    #dots{
       position: absolute;
       bottom: 10px;
       right: calc(50% - 40px);
    }
   
    .square{
        width: 20px;
        height: 8px;
        margin: 10px;
        display: inline-block;
    }
    .active{
        position: relative;
        bottom: 6px;
    }

    #line{
        width: 50px;
        height: 1px;
        border-bottom: 1px white solid;
        opacity: 0.6;
    }
</style>