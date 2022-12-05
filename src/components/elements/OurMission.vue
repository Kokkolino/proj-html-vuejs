<template>
    <div id="container">
        <!-- our philosophy -->
        <section id="details">
            <!-- comments -->
            <div id="commentCont">
                <div class="comment" :class="[pointer == 1 ? 'active' : '']"
                @click="pointer = 1">
                    <span>Overview</span>
                    <div class="tail"></div>
                </div>
                <div class="comment" :class="[pointer == 2 ? 'active' : '']"
                @click="pointer = 2">
                    <span>Our Mission</span>
                    <div class="tail"></div>
                </div>
            </div>
            <!-- big title -->
            <h2>Our philosophy is learning through play as we offer a stimulating enviroment for children.</h2>
            <!-- upper circle section -->
            <div v-if="pointer == 1" class="circleSect">
                <span class="circle"><img src="../../assets/img/clock_alt.png" alt=""></span>
                <div>
                    <h3>Full Day Sessions</h3>
                    <p>Morbi vestibulum ante sem, vel ullamcorper lectus dignissim eget. Proin ut ligula a purus commodo malesuada id et purus.</p>
                </div>
            </div>
            <div v-else-if="pointer == 2" class="circleSect">
                <span class="circle"><img src="../../assets/img/bell_alt.png" alt=""></span>
                <div>
                    <h3>ipsum lorem</h3>
                    <p>Morbi vestibulum ante sem, vel ullamcorper lectus dignissim eget. Proin ut ligula a purus commodo malesuada id et purus.</p>
                </div>
            </div>
            <!-- lower circle section -->
            <div v-if="(pointer == 1)" class="circleSect">
                <span class="circle"><img src="../../assets/img/diagram_alt.png" alt=""></span>
                <div>
                    <h3>Varied Classes</h3>
                    <p>Morbi vestibulum ante sem, vel ullamcorper lectus dignissim eget. Proin ut ligula a purus commodo malesuada id et purus.</p>
                </div>
            </div>
            <div v-else-if="(pointer == 2)" class="circleSect">
                <span class="circle"><img src="../../assets/img/globe_alt.png" alt=""></span>
                <div>
                    <h3>lorem ipsum</h3>
                    <p>Morbi vestibulum ante sem, vel ullamcorper lectus dignissim eget. Proin ut ligula a purus commodo malesuada id et purus.</p>
                </div>
            </div>
        </section>
        <!-- ---- -->
        <!-- slider -->
        <section id="slider">

            <MissionSlider/>

        </section>
    </div>
</template>

<script>
import MissionSlider from "./MissionSlider.vue"

    export default {
        name: 'OurMission',
        components: {
            MissionSlider
        },
        data(){
            return {
                pointer: 1,
            }
        },
    }
</script>

<style lang="scss" scoped>
    #container{
        display: flex;
        justify-content: space-between;
    }

    section {
        width: 50%;
        padding: 10px;
    }

    #details{
        display: flex;
        flex-direction: column;
        text-align: start;
        padding-right: 50px;
        p{
            opacity: 0.5;
            font-weight: 500;
        }
    }   

    #commentCont{
        display: flex;
        justify-content: flex-start;
        gap: 25px;
        margin-bottom: 15px;
    }
    .comment {
        padding: 15px;
        position: relative;
        z-index: 2;
        cursor: pointer;
        box-shadow: 3px 6px 9px #888888;
    }

    .active{
        background-color: #fe6601;
        .tail{
            display: block;
        }
    }
    .tail{
        position: absolute;
        width: 26px;
        height: 26px;
        transform: rotate(45deg);
        background-color: #fe6601;
        bottom: -5px;
        left: calc(50% - 13px);
        z-index: -1;
        display: none;
    }

    h2, h3{
        color: #554e9e;
        font-weight: 500;
        margin-bottom: 20px;
    }

    .circleSect{
        display: flex;
        margin-bottom: 30px;
        div{
            width: calc(100% - 80px);
            padding-left: 20px;
        }
    }
    .circle{
        display: flex;
        justify-content: center;
        align-items: center;
        width: 80px;
        height: 80px;
        border-radius: 50%;
        background-color: #fe6601;
    }

    // slider
    #slider{
        width: 45%;
    }
</style>