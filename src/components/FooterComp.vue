<template>
    <div >
        <section class="w-50" style="margin-bottom: 50px">
            <ContactElem
            :contacts="contacts"/>
        </section>
        <form class="w-50">

            <section id="inputSect" v-on:submit.prevent>
                <div class="inputCont">
                    <input type="text" placeholder="Your Name *" required>
                </div>
                <div class="inputCont">
                    <input type="email" placeholder="Your E-mail *" required>
                </div>
                <div class="inputCont">
                    <input type="text" placeholder="Subject">
                </div>

            </section>
            <section id="textArea">
                <div>
                    <textarea name="message" id="" cols="100%" rows="100%" placeholder="Your Message *" required></textarea>
                </div>
            </section>
            <button>SEND MESSAGE</button>
        </form>
        <!-- about us -->
        <section id="about">
            <div id="sectCont" class="w-50">
                <div class="aboutCont">
                    <h3>
                        ABOUT US
                    </h3>
                    <div class="head">
                    </div>
                        <P>
                            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Soluta obcaecati laboriosam magni vitae iure optio quasi
                        </P>
                </div>

                <div class="aboutCont">
                    <h3>ARCHIVES</h3>
                    <div class="head">
                    </div>  
                    <div class="months">OCTOBER 2014(2)</div>
                    <div class="months">SEPTEMBER 2014(2)</div>
                    <div class="months">AUGUST 2014(2)</div>
                    <div class="months">JULY 2014(2)</div>
                    <div class="months">JUNE 2014(2)</div>
                    <div class="months">MAY 2014(1)</div>
                </div>

                <div class="aboutCont">
                    <h3>OUR FEATURES</h3>
                    <div class="head">
                    </div>
                    <span>
                        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Rerum minima natus officiis?
                        <ul>
                            <li>Friendly and welcoming place</li>
                            <li>Science and art classes</li>
                            <li>Positive learning environment</li>
                            <li>Educational field trips</li>
                            <li>Writing and reading classes</li>
                            <li>Science and art classes</li>
                        </ul>
                    </span>
                </div>

                <div id="recent" class="aboutCont">
                    <h3>RECENT POSTS</h3>
                    <div class="head">
                    </div>
                    <RecentPosts
                    v-for="(elem, index) in news"
                    :key="index"
                    :posts="elem"/>
                </div>
            </div>
        </section>
        <footer>
            <div id="socials">
                <span>
                    <img src="../assets/img/behance.png" alt="">
                </span>
                <span>
                    <img src="../assets/img/dribbble.png" alt="">
                </span>
                <span>
                    <img src="../assets/img/envato.png" alt="">
                </span>
                <span>
                    <img src="../assets/img/facebook.png" alt="">
                </span>
                <span>
                    <img src="../assets/img/twitter.png" alt="">
                </span>
            </div>
            <div>
                © Fable - Children Kindergarten WordPress Theme by QuinticaLabs
            </div>
        </footer>
    </div>
</template>

<script>
import ContactElem from './elements/ContactElem.vue';
import RecentPosts from "./elements/RecentPosts.vue"

    export default {
        name: 'FooterComp',
        components: {
            ContactElem,
            RecentPosts
        },
        data(){
            return{
                contacts: [
                    {
                        img: "envelope (1).png",
                        title: "Postal Address",
                        data1: {
                            string: true,
                            info: "Fable Care Center",
                        },
                        data2: {
                            string: true,
                            info: "85 Fentiman Ave",
                        },
                        data3: {
                            string: true,
                            info: "Ottawa, ON K1S 0T7",
                        }
                    },
                    {
                        img: "mobile.png",
                        title: "Phone & E-mail",
                        data1: {
                            string: true,
                            info: "Phone: 1-800-64-38",
                        },
                        data2: {
                            string: true,
                            info: "Fax: 1-800-64-39",
                        },
                        data3: {
                            string: false,
                            info: "office@fable.com",
                        }
                    },
                    {
                        img: "clock.png",
                        title: "Business Hours",
                        data1: {
                            string: true,
                            info: "Monday - Friday",
                        },
                        data2: {
                            string: true,
                            info: "8:00am - 5:00pm",
                        },
                        data3: {
                            string: true,
                            info: "Weekend Closed",
                        }
                    },
                    {
                        img: "document (1).png",
                        title: "Sessions",
                        data1: {
                            string: true,
                            info: "Mornings, 9 am - 12 noon",
                        },
                        data2: {
                            string: true,
                            info: "Afternoons, 1 pm - 5 pm",
                        },
                        data3: {
                            string: true,
                            info: "Full Day, 8 am - 5 pm",
                        }
                    }



                ]
            }
        },
        props: {
            news: Array
        }
    }
</script>

<style lang="scss" scoped>
    form{
        margin-top: 50px;
        margin-bottom: 50px;
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        section{
            flex-basis: calc(50% - 20px);
            height: 200px;
            input{
                border: none;
                width: 90%;
            }
        }
        .inputCont{
            width: 100%;
            height: 40px;
            border: 1px solid #e8e6e7;
            text-align: start;
            padding: 10px;
        }
    }

    #inputSect{
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }

    #textArea{
        div{
            width: 100%;
            height: 100%;
            border: 1px solid #e8e6e7;
            textarea{
                max-width: 540px;
                max-height: 100%;
                resize: none;
            }
        }
    }

    button{
        justify-self: center;
        margin: 30px auto;
        background-color: #fe6601;
        border: none;
        color: white;
        padding: 10px;
    }

    #about{
        height: 50vh;
        background-image: url("../assets/img/pattern.png");
        padding: 50px;
        text-align: start;
        color: white;
    }

    .aboutCont{
        flex-basis: calc((100% / 4) - 40px);
    }

    #sectCont{
        display: flex;
        justify-content: space-between;

    }

    .head{
        height: 1px;
        width: 30%;
        border: 1px solid white;
        opacity: 0.6;
        margin-top: 6px;
        margin-bottom: 20px;
    }
    .months{
        border: 1px solid rgba($color: #ffffff, $alpha: 0.6);
        width: 100%;
        height: 40px;
        margin-bottom: 5px;
        display: flex;
        justify-content: start;
        align-items: center;
        padding: 10px;
        font-size: 15px;
        font-weight: 600;
        cursor: pointer;
    }

    #about ul{
        list-style-image: url("../assets/img/style_4_alt.png");
        list-style-position: inside;
        margin: 20px 0;
        
    }

    #recent{
        *{
            margin-bottom: 10px;
        }
    }
    footer{
        height: 15vh;
        display: flex;
        justify-content: center;
        flex-direction: column;
        align-items: center;
        gap: 20px;

        #socials{
            display: flex;
            gap: 3px;
            
            span{
                background-color: #fe6601;
                height: 45px;
                width: 45px;
                cursor: pointer;
                display: flex;
                align-items: center;
                justify-content: center;
            }
        }
    }
</style>