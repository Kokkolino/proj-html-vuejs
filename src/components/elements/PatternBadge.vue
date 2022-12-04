<template>
    <section class="w-100">
        <div class="w-50 f-bw">
            <h1>{{title}}</h1>
            <button>{{btn}}</button>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'PatternBadge',
        props: {
            title: String,
            btn: String,
        }
    }
</script>

<style lang="scss" scoped>
    section{
        height: 150px;
        background-image: url("../../assets/img/pattern.png");
        color: white;
    }

    div{
        height: 100%;
    }
    
    h1{
        font-size: 33px;
        font-weight: lighter;
    }

    button{
        font-weight: bolder;
        color: white;
        background: none;
        border: 2px solid white;
        padding: 14px;
        cursor: pointer;
    }
</style>