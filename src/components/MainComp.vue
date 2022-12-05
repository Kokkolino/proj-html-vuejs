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
        
    </div>
</template>

<script>
import SliderElem from "./elements/SliderElem.vue"
import PatternBadge from "./elements/PatternBadge.vue"
import SectSplitter from "./elements/SectSplitter.vue"
import CirclesElem from "./elements/CirclesElem.vue"
import OurMission from "./elements/OurMission.vue"
import ParallaxElem from "./elements/ParallaxElem.vue"

    export default {
        name: 'MainComp',
        components: {
            SliderElem,
            PatternBadge,
            SectSplitter,
            CirclesElem,
            OurMission,
            ParallaxElem
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
</style>