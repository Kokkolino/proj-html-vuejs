<template>
    <div>
        <!-- image -->
        <div id="container">
            <section id="imageSect">
                <img id="image" :src="require(`../../assets${card.img}`)" alt="">
                <div class="quote">
                    <img src="../../assets/img/quote.png" alt="">
                </div>
            </section>
            <!-- description -->
            <section id="description">
                <p>{{card.bio}}</p>
            </section>
        </div>
        <div id="container2">
            <section>
            <h2>{{card.title}}</h2>
            <h6>{{card.role}}</h6>

            </section>
            <section id="socials">
                <span class="social">
                    <img :src="require(`../../assets/img${card.social[0]}`)" alt="">
                </span>
                <span class="social">
                    <img :src="require(`../../assets/img${card.social[1]}`)" alt="">
                </span>
                <span class="social">
                    <img :src="require(`../../assets/img${card.social[2]}`)" alt="">
                </span>

            </section>
        </div>
    </div>
</template>

<script>
    export default {
        name: "StaffCard",
        props: {
            card: Object,
        }
    }
</script>

<style lang="scss" scoped>
    #container {
        width: 100%;
        display: flex;
        flex-wrap: wrap;
    }

    p{
        opacity: 0.6;
        text-align: start;
    }

    #container2{
        display: flex;
        flex-wrap: wrap;
        h2{
            font-weight: 100;
            color: #554e9e;
        }
        h6{
            opacity: 0.6;
        }
    }
    section{
        flex-basis: 50%;
    }

    #imageSect{
        background-size: contain;
        position: relative;
        #image{
            height: 200px;
        }
    }

    .quote{
        height: 40px;
        width: 120px;
        color: white;
        border: 1px solid #fe6601;
        padding: 10px;
        display: flex;
        justify-content: flex-end;
        align-items: center;
        cursor: pointer;
        img{
            height: 32px;
            width: 32px;
        }
        position: absolute;
        top: 30px;
        right: -60px;
    }

    #description{
        padding-top: 80px;
    }

    #socials{
        display: flex;
        gap: 10px;
    }
    .social{
        cursor: pointer;
        background-color: #fe6601;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 40px;
    }
</style>