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
        <!-- splitter img -->
        <section id="splitterImg">
            <img src="../assets/img/gallery_01-690x506.jpg" alt="">
            <img src="../assets/img/gallery_02-690x506.jpg" alt="">
            <img src="../assets/img/gallery_03-690x506.jpg" alt="">
            <img src="../assets/img/gallery_04-690x506.jpg" alt="">
        </section>
        <PatternBadge
        title="See Our Kindergarten Photo Gallery"
        btn="VIEW GALLETY >"
        />
        <SectSplitter
        title="Meet Our Staff"
        description="With education and experience in early childhood care"/>
        <section class="w-50">
            <div id="staffTop">
                <h1>Our staff consists of three teachers and one assistant with experience in early childhood care</h1>

                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat nostrum dolor beatae, blanditiis dolorum, ut alias sapiente velit architecto, necessitatibus reiciendis at porro earum quisquam doloremque aspernatur rem ea animi.</p>
            </div>
            <div id="staffBot">
                <StaffCard
                v-for="(elem, index) in staff"
                :key="index"
                :card="elem"/>
            </div>
        </section>
        <section style="height: 50vh;">
            <ParallaxElem2
            :slides="slide3"
            :quotes="quotes"
            color="white"/>
        </section>
        <SectSplitter
        title="What's New"
        description="Keep up to date with the latest news"/>
        <!-- News -->
        <section id="blog" class="w-50">
            <div id="news">
                <NewsCard
                class="news-card"
                v-for="(elem, index) in news1"
                :key="index"
                :news="elem"
                />
            </div>
            <div>
                <button>
                    GO TO BLOG >
                </button>
            </div>
        </section>
        <!-- maps -->
        <section style="height: 380px; margin-bottom: 60px;">
            <MapElem/>
        </section>
        <SectSplitter
        title="Contact Us"
        description="Our postal address and contact details"/>
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
import StaffCard from "./elements/StaffCard.vue"
import ParallaxElem2 from "./elements/ParallaxElem2.vue"
import NewsCard from "./elements/NewsCard.vue"
import MapElem from "./elements/MapElem.vue"

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
            StaffCard,
            ParallaxElem2,
            NewsCard,
            MapElem
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

                ],
                staff:[
                    {
                        img: "/img/team_01.jpg",
                        title: "Ruth Richie",
                        role: "Teacher",
                        bio: "I have just finished my studies in Early Childhood Education and I am also the kid's yoga teacher here at Fable. I enjoy cooking, swimming and bike riding in my free time",
                        social:[
                            "/mail.png",
                            "/facebook.png",
                            "/pinterest.png"
                        ]

                        
                    },
                    {
                        img: "/img/team_02.jpg",
                        title: "Katie Willmore",
                        role: "Assistant Teacher",
                        bio: "My name is Katie. I grew up and studied in Canada. This is my second year at Fable and love every minute of it, making the children's learning experience fun.",
                        social:[
                            "/dribbble.png",
                            "/stumbleupon.png",
                            "/instagram.png"
                        ]
                    },
                    {
                        img: "/img/team_03.jpg",
                        title: "Angelica Watson",
                        role: "Lead Teacher",
                        bio: "I hold a degree in Early Childhood Education and an advanced English language certificate. I have been working as a kindergarten teacher since 2002.",
                        social:[
                            "/bing.png",
                            "/skype.png",
                            "/linkedin.png"
                        ]
                    },
                    {
                        img: "/img/team_04.jpg",
                        title: "Angel Lynn",
                        role: "Teacher",
                        bio: "I have completed a Graduate Diploma in Early Childhood Teaching. I have worked with children aged from six weeks to eight years. This is my second year at Fable.",
                        social:[
                            "/bing.png",
                            "/skype.png",
                            "/linkedin.png"
                        ]
                    },


                ],
                slide3:[
                    "/img/parallax_01.jpg",
                    "/img/parallax_02.jpg"
                ],
                quotes:[
                    {
                        quote: "Fable Kindergarten is a great place for my daughter to start her schooling experience. It's welcoming and safe and my daughter loves being there",
                        author:"Joe R. Hamblen"
                    },
                    {
                        quote: "lorem ipsum dolor sit amet, consectet, ",
                        author:"Ipsum Lorem"
                    }

                ],
                news1:[
                    {
                        date: "October 03, 2014",
                        img: "img/blog_09.jpg",
                        number: "42",
                        title: "Drawing and Painting Lessons",
                        author:"Anna Brown",
                        genre: "Events, Fun",
                        article: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer non dapibus augue. Praesent quam nisi, elementum at porttitor vel, lacinia sit amet enim. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Aenean a facilisis justo. Etiam rutrum egestas leo nec rutrum. Fusce massa metus, vestibulum vel metus et, rutrum varius sem. Proin sit amet leo vel lacus vestibulum aliquet nec et neque. Phasellus egestas dui tellus. Curabitur semper imperdiet nibh et ornare. Curabitur nec magna dolor. Aenean faucibus ligula arcu, id placerat metus tincidunt id. Integer sodales auctor semper. Nunc id ligula sit amet odio lacinia rutrum. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Integer dolor tortor, lobortis vitae purus id, ornare ullamcorper felis."
                    },
                    {
                        date: "October 03, 2014",
                        img: "img/blog_10.jpg",
                        number: "19",
                        title: "Fall Parents Meeting Day",
                        author:"Anna Brown",
                        genre: "Dance, Education",
                        article: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer non dapibus augue. Praesent quam nisi, elementum at porttitor vel, lacinia sit amet enim. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Aenean a facilisis justo. Etiam rutrum egestas leo nec rutrum. Fusce massa metus, vestibulum vel metus et, rutrum varius sem. Proin sit amet leo vel lacus vestibulum aliquet nec et neque. Phasellus egestas dui tellus. Curabitur semper imperdiet nibh et ornare. Curabitur nec magna dolor. Aenean faucibus ligula arcu, id placerat metus tincidunt id. Integer sodales auctor semper. Nunc id ligula sit amet odio lacinia rutrum. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Integer dolor tortor, lobortis vitae purus id, ornare ullamcorper felis."
                    },
                    {
                        date: "October 03, 2014",
                        img: "img/blog_08.jpg",
                        number: "22",
                        title: "Fall Parents Meeting Day",
                        author:"Anna Brown",
                        genre: "Games, General",
                        article: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer non dapibus augue. Praesent quam nisi, elementum at porttitor vel, lacinia sit amet enim. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Aenean a facilisis justo. Etiam rutrum egestas leo nec rutrum. Fusce massa metus, vestibulum vel metus et, rutrum varius sem. Proin sit amet leo vel lacus vestibulum aliquet nec et neque. Phasellus egestas dui tellus. Curabitur semper imperdiet nibh et ornare. Curabitur nec magna dolor. Aenean faucibus ligula arcu, id placerat metus tincidunt id. Integer sodales auctor semper. Nunc id ligula sit amet odio lacinia rutrum. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Integer dolor tortor, lobortis vitae purus id, ornare ullamcorper felis."
                    }

                ],
                mapPuzzle: [
                    "/vt.png",
                    "/vt (1).png",
                    "/vt (2).png",
                    "/vt (3).png",
                    "/vt (4).png",
                    "/vt (5).png",
                    "/vt (6).png",
                    "/vt (7).png",
                    "/vt (8).png",
                    "/vt (9).png",
                    "/vt (10).png",
                    "/vt (11).png",
                    "/vt (12).png",
                    "/vt (13).png",
                    "/vt (14).png",
                    "/vt (15).png",
                    "/vt (16).png",
                    "/vt (17).png",
                    "/vt (18).png",
                    "/vt (19).png",
                    "/vt (20).png",
                    "/vt (21).png",
                    "/vt (22).png",
                    "/vt (23).png",
                    "/vt (24).png",
                    "/vt (25).png",
                    "/vt (26).png",
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
        height:70vh; 
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

    #splitterImg{
        img{
            width: 25%;
        }
        margin-bottom: -4px;
    }

    #staffTop{
        display: flex;
        justify-content: space-between;
        *{
            flex-basis: calc(50% - 20px);
        }
        h1{
            color: #554e9e;
            font-weight: 100;
        }
        p{
            opacity: 0.6;
            font-weight: 600;
        }
    }

    #staffTop, #staffTop{
        margin-bottom: 50px;
    }

    #staffBot{
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        gap: 20px;
        margin-bottom: 60px;
    }

    #staffBot > *{
        margin-bottom: 10px;
        flex-basis: calc(50% - 20px);
    }

    #news{
        display: flex;
        justify-content: space-between;
        margin-bottom: 50px;
    }
    .news-card{
        width: calc((100% / 3) - 100px);
    }

    #blog{
        margin-bottom: 50px;
        button{
            padding: 10px;
            color: white;
            border: none;
            background-color: #fe6601;
            cursor: pointer;
        }
    }
    #map{
        display: flex;
        flex-wrap: wrap;
        flex-direction: column;
        height: 750px;
        img{
            width: 250px;
            height: 250px;
        }
    }
</style>