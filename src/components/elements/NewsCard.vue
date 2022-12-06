<template>
    <div id="container">
        <div id="date">
            {{news.date}}
        </div>
        <div id="img" :style='{backgroundImage: "url("+require(`../../assets/${news.img}`) +`)`,}'>
            <span>
                {{news.number}}
            </span>
        </div>
        <h3>{{news.title}}</h3>
        <p>
            <span>
                {{beforeLoad}}
            </span>
            <span id="more" v-show="!loaded" @click="showMore()">[...]</span>
            <span id="load" v-show="loaded">
                {{afterLoad}}
            </span>
            <span id="less" v-show="loaded" @click="showMore()">
                [...]
            </span>
        </p>
        <div id="line"></div>
        <div id="credits">
            <div id="author">
                <img src="../../assets/img/author.png" alt="">
                <span>
                {{news.author}}
                </span>
            </div>
            <div id="genre">
                <img src="../../assets/img/category.png" alt="">
                <span>
                    {{news.genre}}
                </span>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'NewsCard',
        props: {
            news: Object,
            size: String,
        },
        data(){
            return{
                beforeLoad:"",
                afterLoad:"",
                loaded: false,
                max: 0
            }
        },
        mounted(){
            this.beforeLoad = this.news.article.slice(0, 150);
            this.max =this.news.article.length - 1;
            this.afterLoad = this.news.article.slice(150, this.max)
        },
        methods: {
            showMore(){
                if(this.loaded == true){
                    return this.loaded = false
                }
                return this.loaded = true
            }
        }
    }
</script>

<style lang="scss" scoped>
    #img{
        width: 100%;
        aspect-ratio: 1/1;
        position: relative;
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        span{
            position: absolute;
            bottom: 0;
            right: 0;
            width: 40px;
            height: 40px;
            background-color: #fe6601;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
        }
    }
    #line{
        width: 100%;
        height: 1px;
        border-bottom: 1px solid black;
        opacity: 0.6;
    }
    #more, #less{
        opacity: 0.6;
        cursor: pointer;
    }
    #date{
        opacity: 0.6;
        text-align: start;
        margin-bottom: 5px;
    }
    h3{
        margin: 20px 0;
        color: #554e9e;
        font-weight: 100;
    }

    p{
        opacity: 0.8;
        margin-bottom: 20px;
    }

    #credits{
        display: flex;
        margin: 10px 0;
    }

    #author, #genre{
        flex-basis: 50%;
        text-align: start;
        span{
            font-size: 13px;
            opacity: 0.6;
            margin-left: 4px;
            vertical-align: middle;
        }
        img{
            vertical-align: middle;
        }
    }
</style>