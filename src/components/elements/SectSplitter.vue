<template>
    <div id="container">
       <h1>{{title}}</h1>
       <p>{{description}}</p>
       <div><img src="../../assets/img/header_divider.png" alt=""></div>
    </div>
</template>

<script>
    export default {
        name: 'SectSplitter',
        props: {
            title: String,
            description: String,
        }
    }
</script>

<style lang="scss" scoped>
    #container {
        height: 200px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        padding: 50px 0 ;
        gap: 20px;
    }

    h1{
        color: #554e9e;
        font-weight: 100;
    }

    p{
        font-weight: bold;
        opacity: 0.4;
    }

    img{
        width: 100px;
    }
</style>