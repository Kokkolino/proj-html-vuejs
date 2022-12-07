<template>
    <div id="container">
        <div v-for="(elem, index) in contacts"
        :key="index">
            <img :src="require(`../../assets/img/${elem.img}`)" alt="">
            <h2>{{elem.title}}</h2>
            <p v-if="elem.data1.string">{{elem.data1.info}}</p>
            <a v-else href="">{{elem.data1.info}}</a>

            <p v-if="elem.data2.string">{{elem.data2.info}}</p>
            <a v-else href="">{{elem.data2.info}}</a>

            <p v-if="elem.data3.string">{{elem.data3.info}}</p>
            <a v-else href="">{{elem.data3.info}}</a>

        </div>
    </div>
</template>

<script>
    export default {
        name: 'ContactElem',
        props: {
            contacts: Array
        }
    }
</script>

<style lang="scss" scoped>
    #container{
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
    }

    h2{
        font-weight: 100;
        color: #554e9e;
        margin: 20px 0;
    }
    p{
        opacity: 0.6;
        font-size: medium;
        margin: 4px 0;
    }
</style>