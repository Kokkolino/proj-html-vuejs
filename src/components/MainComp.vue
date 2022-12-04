<template>
    <div>
        <section id="slider3">
            <div>
                <SliderElem
                :slides="slide1"
                />
            </div>
        </section>
        <PatternBadge
        title="How to Enroll Child to a Class?"
        btn="LEARN MORE >"
        />
        <SectSplitter
        title="Welcome to Fable"
        description="Fable daycare, preschool, and kindergarten"/>
    </div>
</template>

<script>
import SliderElem from "./elements/SliderElem.vue"
import PatternBadge from "./elements/PatternBadge.vue"
import SectSplitter from "./elements/SectSplitter.vue"

    export default {
        name: 'MainComp',
        components: {
            SliderElem,
            PatternBadge,
            SectSplitter,
        },
        data(){
            return {
                slide1: [
                    "/img/slider_slide3_img1.png",
                    "/img/slider_slide3_img2.png",
                    "/img/slider_slide3_img3.png",
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    #slider3{
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
</style>