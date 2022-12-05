<template>
    <section id="container" class="w-100 f-bw">
        <!-- first circle -->
        <div class="elemContainer">
            <div class="circles" :class="[circles[0].border == true ? 'bordered' : 'borderless']" :style="{backgroundColor: circles[0].bg}">
                <img v-if="circles[0].img==true" :src="require(`../../assets/img${circles[0].imgPath}`)">
                <h1 v-else>{{circles[0].innerh}}</h1>
            </div>
            <h3 :style="{color: circles[0].hcolor, opacity: circles[0].hopacity}">
                {{circles[0].title}}
            </h3>
            <p :style="{opacity: circles[0].dopacity, color: circles[0].dcolor}">
                {{circles[0].description}}
            </p>
        </div>
        <!-- second circle -->
        <div class="elemContainer">
            <div class="circles" :class="[circles[1].border == true ? 'bordered' : 'borderless']" :style="{border:circles[1].bord, backgroundColor: circles[1].bg}">
                <img v-if="circles[1].img==true" :src="require(`../../assets/img${circles[1].imgPath}`)">
                <h1 v-else>{{circles[1].innerh}}</h1>
            </div>
            <h3 :style="{color: circles[1].hcolor, opacity: circles[1].hopacity}">
                {{circles[1].title}}
            </h3>
            <p :style="{opacity: circles[1].dopacity, color: circles[1].dcolor}">
                {{circles[1].description}}
            </p>
        </div>
        <!-- third circle -->
        <div class="elemContainer">
            <div class="circles" :class="[circles[2].border == true ? 'bordered' : 'borderless']" :style="{border:circles[2].bord, backgroundColor: circles[2].bg}">
                <img v-if="circles[2].img==true" :src="require(`../../assets/img${circles[2].imgPath}`)">
                <h1 v-else>{{circles[2].innerh}}</h1>
            </div>
            <h3 :style="{color: circles[2].hcolor, opacity: circles[2].hopacity}">
                {{circles[2].title}}
            </h3>
            <p :style="{opacity: circles[2].dopacity, color: circles[2].dcolor}">
                {{circles[2].description}}
            </p>
        </div>
        <!-- fourth circle -->
        <div class="elemContainer">
            <div class="circles" :class="[circles[3].border == true ? 'bordered' : 'borderless']" :style="{border:circles[3].bord, backgroundColor: circles[3].bg}">
                <img v-if="circles[3].img==true" :src="require(`../../assets/img${circles[3].imgPath}`)">
                <h1 v-else>{{circles[3].innerh}}</h1>
            </div>
            <h3 :style="{color: circles[3].hcolor, opacity: circles[3].hopacity}">
                {{circles[3].title}}
            </h3>
            <p :style="{opacity: circles[3].dopacity, color: circles[3].dcolor}">
                {{circles[3].description}}
            </p>
        </div>



    </section>
</template>

<script>
    export default {
        name: 'CirclesElem',
        props: {
            circles: Array
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

    .circles{
        border-radius: 50%;
        height: 150px;
        width: 150px;
       display: flex;
       justify-content: center;
       align-items: center;
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