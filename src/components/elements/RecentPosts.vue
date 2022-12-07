<template>
    <div id="container">
        <div>
            <img :src="require(`../../assets/${posts.img}`)" alt="">
        </div>
        <div id="info">
            <h4>{{posts.title}}</h4>
            <ul>
                <li>
                    {{posts.date}}
                </li>
            </ul>
            
        </div>
    </div>
</template>

<script>
    export default {
        name: 'RecentPosts',
        props: {
            posts: Object
        }
    }
</script>

<style lang="scss" scoped>
    #container{
        height: 80px;
        width: 100%;
        display: flex;
    }

    img{
        height: 100%;
        aspect-ratio: 1/1;
    }

    #info{
        padding-left: 20px;
        ul{
            margin-top: 8px;
            list-style-image: url("../../assets/img/date_footer.png");
            list-style-position: inside;
        }
    }
</style>