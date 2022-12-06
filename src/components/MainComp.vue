<template>
    <div>
        <!-- sliders 1 -->
        <section id="slider1">
            <div>
                <SliderElem
                :slides="slide1"
                color="#fe6601"
                />
            </div>
        </section>
        <!-- badge -->
        <PatternBadge
        title="How to Enroll Child to a Class?"
        btn="LEARN MORE >"
        />
        <SectSplitter
        title="Welcome to Fable"
        description="Fable daycare, preschool, and kindergarten"/>
        <!-- circles section -->
        <div class="w-50">
            <CirclesElem
            :circles="circles1"
            />
        </div>
        <!-- Our mission section -->
        <section class="w-100" style="background-color: #e8e6e7; padding-top: 30px;">
            <div class="w-50">
                <OurMission/>
            </div>
        </section>
        <!-- Our Pupils -->
        <section id="pupils">
            <ParallaxElem
            :slides="slide2"
            color="white"
            :circles="circles2"/>
        </section>
        <SectSplitter
        title="Our Classes"
        description="Our preschool program has four dedicated classes"
        />
        <!-- our classes -->
        <section style="height:50vh">
            <div id="classesHeader" class="w-50" >
                <h1>We provided four classes with nine to twenty children each aged twelve month to five years of age.</h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta voluptate asperiores, quas ducimus similique atque aliquid fugit et eveniet provident ea. Corporis aliquid ex, eum excepturi impedit sit minus nemo!</p>
            </div>
            <div id="classes" class="w-50">
                <CardsElem
                v-for="(elem, index) in cards"
                :card="elem"
                :key="index"/>
            </div>
        </section>
        <!-- our goals -->
        <section id="goals">
            <section class="w-50">
                <div id="leftGoal">
                    <h1>We have been educating children for over fifteen years. Our goal is to create a place that engages each child.</h1>
                    <p id="a">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Beatae vero illum aspernatur, reprehenderit doloremque ullam sit dolor dolorum saepe, rem iure ex laboriosam error voluptas obcaecati non temporibus laborum ab.</p>
                    <ul>
                        <li>
                            <p>Comprehensive reporting on individual achievement</p>
                        </li>
                        <li>
                            <p> Educational field trips and school presentations</p>
                        </li>
                        <li>
                            <p>Individual attention in a small-class setting</p>
                        </li>
                        <li>
                            <p>Learning program with after-school care</p>
                        </li>
                        <li>
                            <p>Opportunities to carry out scientific investigations</p>
                        </li>
                        <li>
                            <p>Positive learning environment for your child</p>
                        </li>
                    </ul>
                </div>
                <div id="rightGoal">
                    <CirclesElem
                    wrap="wrap"
                    :circles="circles3"/>
                </div>
            </section>
        </section>
    </div>
</template>

<script>
import SliderElem from "./elements/SliderElem.vue"
import PatternBadge from "./elements/PatternBadge.vue"
import SectSplitter from "./elements/SectSplitter.vue"
import CirclesElem from "./elements/CirclesElem.vue"
import OurMission from "./elements/OurMission.vue"
import ParallaxElem from "./elements/ParallaxElem.vue"
import CardsElem from "./elements/CardsElem.vue"

    export default {
        name: 'MainComp',
        components: {
            SliderElem,
            PatternBadge,
            SectSplitter,
            CirclesElem,
            OurMission,
            ParallaxElem,
            CardsElem,
        },
        data(){
            return {
                slide1: [
                    "/img/slider_slide3_img1.png",
                    "/img/slider_slide3_img2.png",
                    "/img/slider_slide3_img3.png",
                ],
                circles1: [
                    {
                        border: false,
                        bg: "#fe6601",
                        img: true,
                        imgPath: "/schoolbag_alt.png",
                        innerh: null,
                        hcolor: "#554e9e",
                        hopacity: "1",
                        title: "Morbi Etos",
                        dcolor: "black",
                        dopacity: "0.5",
                        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean imperdiet urna vel metus suscipit mattis. "
                    },
                    {
                        border: false,
                        bg: "#554e9e",
                        img: true,
                        imgPath: "/stroller_alt.png",
                        innerh: null,
                        hcolor: "#554e9e",
                        hopacity: "1",
                        title: "Congue Gravida",
                        dcolor: "black",
                        dopacity: "0.5",
                        description: "Morbi vestibulum ante sem, vel ullamcorper lectus dignissim eget. Proin ut ligula a purus commodo malesuada id et purus."
                    },
                    {
                        border: false,
                        bg: "#fe6601",
                        img: true,
                        imgPath: "/globe_alt.png",
                        innerh: null,
                        hcolor: "#554e9e",
                        hopacity: "1",
                        title: "Maecenas Node",
                        dcolor: "black",
                        dopacity: "0.5",
                        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean imperdiet urna vel metus suscipit mattis. "
                    },
                    {
                        border: false,
                        bg: "#554e9e",
                        img: true,
                        imgPath: "/bell_alt.png",
                        innerh: null,
                        hcolor: "#554e9e",
                        hopacity: "1",
                        title: "Praesent Morbi",
                        dcolor: "black",
                        dopacity: "0.5",
                        description: "Morbi vestibulum ante sem, vel ullamcorper lectus dignissim eget. Proin ut ligula a purus commodo malesuada id et purus."
                    }
                ],
                slide2:[
                    "/img/parallax_01.jpg",
                    "/img/parallax_02.jpg"
                ],
                circles2: [
                    {
                        border: true,
                        bg: null,
                        img: false,
                        imgPath: null,
                        innerh: "507",
                        hcolor: "white",
                        hopacity: "1",
                        title: "Our Pupils",
                        dcolor: "white",
                        dopacity: "1",
                        description: "Aenean imperdiet urna vel metus suscipit mattis. "
                    },
                    {
                        border: true,
                        bg: null,
                        img: false,
                        imgPath: null,
                        innerh: "235",
                        hcolor: "white",
                        hopacity: "1",
                        title: "Teaching Hours",
                        dcolor: "white",
                        dopacity: "1",
                        description: "Proin ut ligula a purus commodo malesuada id et purus."
                    },
                    {
                        border: true,
                        bg: null,
                        img: false,
                        imgPath: null,
                        innerh: "100%",
                        hcolor: "white",
                        hopacity: "1",
                        title: "Satified Parents",
                        dcolor: "white",
                        dopacity: "1",
                        description: "Aenean imperdiet urna vel metus suscipit mattis. "
                    },
                    {
                        border: true,
                        bg: null,
                        img: false,
                        imgPath: null,
                        innerh: "1050",
                        hcolor: "white",
                        hopacity: "1",
                        title: "Meals Per Year",
                        dcolor: "white",
                        dopacity: "1",
                        description: "Proin ut ligula a purus commodo malesuada id et purus."
                    }
                ],
                cards:[
                    {
                        img: "/img/class_01-690x506.jpg",
                        title: "Little Lambs",
                        years: "Month",
                        old: "12-23",
                        size: "9"
                    },
                    {
                        img: "/img/class_02-690x506.jpg",
                        title: "Bouncy Bears",
                        years: "Year",
                        old: "2-3",
                        size: "12"
                    },
                    {
                        img: "/img/class_03-690x506.jpg",
                        title: "Tenderhearts",
                        years: "Year",
                        old: "3-4",
                        size: "15"
                    },
                    {
                        img: "/img/class_04-690x506.jpg",
                        title: "Shining Stars",
                        years: "Year",
                        old: "4-5",
                        size: "20"
                    },



                ],
                circles3:[
                    {
                        border: false,
                        bg: "white",
                        img: true,
                        imgPath: "/toy.png",
                        innerh: null,
                        hcolor: "#554e9e",
                        hopacity: "1",
                        title: "Learning & Fun",
                        dcolor: "black",
                        dopacity: "0.6",
                        description: " Aenean imperdiet urna vel metus suscipit mattis. "
                    },
                    {
                        border: false,
                        bg: "white",
                        img: true,
                        imgPath: "/meal.png",
                        innerh: null,
                        hcolor: "#554e9e",
                        hopacity: "1",
                        title: "Healthy Meals",
                        dcolor: "black",
                        dopacity: "0.6",
                        description: "Proin ut ligula a purus commodo malesuada id et purus."
                    },
                    {
                        border: false,
                        bg: "white",
                        img: true,
                        imgPath: "/school.png",
                        innerh: null,
                        hcolor: "#554e9e",
                        hopacity: "1",
                        title: "Friendly place",
                        dcolor: "black",
                        dopacity: "0.6",
                        description: "Aenean imperdiet urna vel metus suscipit mattis. "
                    },
                    {
                        border: false,
                        bg: "white",
                        img: true,
                        imgPath: "/shield.png",
                        innerh: null,
                        hcolor: "#554e9e",
                        hopacity: "1",
                        title: "Children Safety",
                        dcolor: "black",
                        dopacity: "0.6",
                        description: "Proin ut ligula a purus commodo malesuada id et purus."
                    }

                ]
            }

        }
    }
</script>

<style lang="scss" scoped>
    #slider1{
        display: flex;
        justify-content: center;
        align-items: flex-end;
        height: 55vh;
        width: 100%;
        background-image: url("../assets/img/slider_slide3_background.png");
        background-size: contain;
        div{
            width: 300px; 
            height: 300px;
        }
    }

    #pupils{
        height: 50vh;
        width: 100%;
    }

    #parallax{
        height: 100%;
        z-index: -1;
    }

    #wcircles{
        z-index: 2;
    }

    #classesHeader{
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
        margin-bottom: 30px;
        *{
            flex-basis:calc(50% - 20px) ;
        }
        h1{
            font-weight: 300;
            color: #554e9e;
        }
        p{
            font-weight: 600;
            opacity: 0.6;

        }
    }

    #classes{
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
        *{
            flex-basis:calc(50% - 20px) ;
        }

    }

    #leftGoal{
        text-align: start;
    }

    #rightGoal{
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        align-items: center;
    }

    #goals{
        height:65vh; 
        background-color:#e8e6e7;
        padding-top: 80px;
        padding-bottom: 80px;
        section{
            display: flex;
            justify-content: space-between;
            div{
                flex-basis: calc(50% - 20px) ;    
                #a{
                    opacity: 0.6;
                }
                h1{
                    color: #554e9e;
                    font-weight: 500;
                    font-size: 25px;

                }
                h1, #a{
                    margin-bottom: 50px;
                    
                }
                ul{
                    list-style-image: url("../assets/img/style_1.png");
                    li{
                        margin-bottom: 6px;
                        text-align: start;
                        p{
                            opacity: 0.6;
                            margin-left: 5px;
                        }
                    }
                }
            }
        }
    }
</style>