<template>
    <section id="container" class="w-100 f-bw" :class="[wrap == 'wrap' ? 'wrap' : '']">
        <!-- first circle -->
        <div class="elemContainer" v-for="(element, index) in circles" :key="index">
            <div class="circles" :class="[element.border == true ? 'bordered' : 'borderless']" :style="{backgroundColor: element.bg}">
                <img v-if="element.img==true" :src="require(`../../assets/img${element.imgPath}`)">
                <h1 v-else>{{element.innerh}}</h1>
            </div>
            <h3 :style="{color: element.hcolor, opacity: element.hopacity}">
                {{element.title}}
            </h3>
            <p :style="{opacity: element.dopacity, color: element.dcolor}">
                {{element.description}}
            </p>
        </div>

    </section>
</template>

<script>
    export default {
        name: 'CirclesElem',
        props: {
            circles: Array,
            wrap: String,
        },
        data(){
            return{

            }
        }
    }
</script>

<style lang="scss" scoped>
    #container {
        gap: 20px;
        align-items: flex-start;
        margin-bottom: 50px;
    }

    .wrap{
        flex-wrap: wrap;
        .elemContainer{
            flex-basis: calc(50% - 20px);
        }
    }

    .circles{
        border-radius: 50%;
        height: 150px;
        width: 150px;
       display: flex;
       justify-content: center;
       align-items: center;
       margin: auto;
    }

    .bordered{
       border: 1px solid white; 
    }

    .borderless{
        border: none;
    }

    h3{
        margin: 15px 0;
    }

    .elemContainer{
        width: 150px;
    }
</style>