<template>
    <div id="container">
        <section id="imgSection" style="background-size: cover;" :style='{backgroundImage: "url("+require(`../../assets${slides[position]}`)}'>
            <div id="alignCont">
                <div class="elemContainer" v-for="(element, index) in circles" :key="index">
                    <div class="circles" :class="[element.border == true ? 'bordered' : 'borderless']" :style="{backgroundColor: element.bg}">
                        <img v-if="element.img==true" :src="require(`../../assets/img${element.imgPath}`)">
                        <h1 :style="{color: color}" v-else>{{element.innerh}}</h1>
                    </div>
                    <h3 :style="{color: element.hcolor, opacity: element.hopacity}">
                        {{element.title}}
                    </h3>
                    <p :style="{opacity: element.dopacity, color: element.dcolor}">
                        {{element.description}}
                    </p>
                </div>
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
            circles: Array
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
    #container {
        width: 100%;
        height: 100%;
    }

    .circles{
        border-radius: 50%;
        height: 150px;
        width: 150px;
       display: flex;
       justify-content: center;
       align-items: center;
    }

    .bordered{
       border: 2px solid white; 
    }

    .borderless{
        border: none;
    }

    h3{
        margin: 15px 0;
    }

    h1{
        font-size: 40px;
        font-weight: 100;
    }

    .elemContainer{
        width: 150px;
    }

    #imgSection{
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
    }

    #alignCont{
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: flex-start;
        min-height: 200px;
        gap: 20px;
        vertical-align: middle;
    }

    #dots{
        position: absolute;
        bottom: 0;
        left: 50%
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

</style>