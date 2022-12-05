<template>
    <div id="container">
        <div id="imgSection">
            <!-- left arrow -->
            <div id="left" @click="slideLeft()" class="arrow"><img src="../../assets/img/go_to_top.png" alt=""></div>
            <!-- img -->
            <img :src="require(`../../assets${photos[position]}`) ">
            <!-- right arrow -->
            <div id="right" class="arrow" @click="slideRight()">
                <img src="../../assets/img/go_to_top.png" alt="">
            </div>
        </div>
        <div id="preview">
            <div>
                <img :src="require(`../../assets${photos[before]}`)" alt="">
            </div>
            <div>
                <img :src="require(`../../assets${photos[position]}`)" alt="">
                <span id="active"></span>
            </div>
            <div>
                <img :src="require(`../../assets${photos[after]}`)" alt="">     
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'MissionSlider',
        data(){
            return{
                before: 0,
                position: 1,
                after: 2,
                photos: [
                    "/img/gallery_01-690x506.jpg",
                    "/img/gallery_07-690x506.jpg",
                    "/img/gallery_08-690x506.jpg"
                ]
            }
        },
        methods:{
            slideLeft(){
            const max = this.photos.length - 1;
           
            
            if(this.before == 0){
                this.before = max;
            }
            else{
                this.before--;
            }

            if(this.position == 0){
                this.position = max;
            }
            else{
                this.position--;
            }

            if(this.after == 0){
                return this.after = max;
            }
            return this.after--;
            },

            slideRight(){
            const max = this.photos.length - 1;
            if(this.before == max){
                this.before = 0;
            }
            else{
                this.before++;
            }

            if(this.position == max){
                this.position = 0;
            }
            else{
                this.position++;
            }

            if(this.after == max){
                return this.after = 0;
            }
            return this.after++;

            }

        }
        
    }
</script>

<style lang="scss" scoped>
    #container{
        width: 100%;
        display: flex;
        flex-wrap: wrap;
    }

    #imgSection{
        position: relative;
        width: 100%;
        img{
            width: 100%;
        }
    }

    .arrow{
        position: absolute;
        width: 50px;
        height: 50px;
        background-color: #fe6601;
        top: calc(50% - 25px);
    }

    #left{
        left: 0;
        img{
            transform: rotate(270deg);
        }
    }

    #right{
        right: 0;
        img{
            transform: rotate(90deg);
        }
    }

    #preview{
        display: flex;
        justify-content: space-between;
        width: 100%;
        div{
            width: calc((100%/ 3) - 6px);
            position: relative;
            img{
                width: 100%;
            }
            
        }
    }

    #active{
        height: 2px;
        width: 100%;
        position: absolute;
        bottom: -6px;
        border-bottom: 2px solid #fe6601;
        left: 0;
    }

</style>