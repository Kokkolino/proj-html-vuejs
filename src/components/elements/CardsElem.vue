<template>
    <div id="container">
        <section id="description">
            <div id="top">
                <h2>{{card.title}}</h2>
                <h6>Class name</h6>
            </div>
            <div id="bottom">
                <div>
                    <h3>{{card.old}}</h3>
                    <h6>{{card.years}} olds</h6>
                </div>
                <div id="line">
                </div>
                <div>
                    <h3>{{card.size}}</h3>
                    <h6>Class size</h6>
                </div>
            </div>
        </section>
        <section id="image" :style='{backgroundImage: "url("+require(`../../assets${card.img}`)}'>
            <div id="read">
                <h5>READ MORE ></h5>
            </div>
        </section>
    </div>
</template>

<script>
    export default {
        name: 'CardsElem',
        props: {
            card: Object
        }
    }
</script>

<style lang="scss" scoped>
    #container {
        display: flex;
        flex-wrap: wrap;
        height: 150px;
    }
    section{
        flex-basis: 50%;
    }

    #image{
        background-size: contain;
        position: relative;
    }

    #read{
        height: 40px;
        width: 120px;
        color: white;
        background-color: #fe6601;
        padding: 10px;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
        h5{
            font-size: 13px;
        }
        position: absolute;
        bottom: 0;
        right: 0;
    }

    #description {
        background-color: #554e9e;
        display: flex;
        padding: 15px;
        flex-wrap: wrap;
        color: white;
    }

    #top{
        flex-basis: 100%;
        text-align: start;
    }

    #bottom{
        flex-basis: 100%;
        align-self: flex-end;
        display: flex;
        justify-content: center;
    }

    #line{
        width: 1px;
        height: 40px;
        border-left: 1px solid white;
        margin: 0 15px;
        opacity: 0.5;
    }

    h2,h3{
        font-weight: normal;
        margin-bottom: 5px;
    }

    h6{
        opacity: 0.6;
        font-weight: normal;
    }
    


</style>