<template>
    <div class="bg-shirt p-5">
        <div class="text-center">
            <h6 class="text-uppercase text-danger">gamer t-shirt's</h6>
            <h1 class="text-uppercase text-white py-3">explore our products</h1>
        </div>
        <div class="box-image container">
            <div class="list d-flex ">
                <div class="card item m-2 mb-5" v-for="(shirt, index) in Tshirt" :key="index">
                    <img :src="shirt.img" alt="">
                    <div class="text-center text-white py-3">
                        <p class="">{{ shirt.title }}</p>
                        <p>{{ shirt.prezzo }}</p>
                        <span class="card-text"></span>
                    <i class="fa solid fa-star voto" v-for="(n, index) in 5" :key="index" 
                    :class="(n <= getRating(shirt.voto) ? 'voto' : 'fa-regular' )" ></i>
                    </div>
                </div>
            </div>
            <hr class="text-light">
        </div>
        <!--section partners-->
        <div class="text-center mt-5">
            <h6 class="text-uppercase text-danger">we our partners</h6>
            <h1 class="text-uppercase text-white py-3">become a partner of gamer</h1>
        </div>
        <div class="parteners text-center container">
            <div class="d-flex flex-wrap justify-content-center">
                <img class="p-5" v-for="path in stemmi" :key="path" :src="path" />
            </div>
            <button type="button" class="btn rounded-0 btn-light 
                    text-uppercase text-danger my-5"> become a partner
                    <i class="fa-solid fa-circle-chevron-right"></i>
            </button>
        </div>
    </div>
</template>

<script>
import { Tshirt } from '../data/data.js';
import { stemmi } from '../data/data.js'
    export default {
        data(){
            return{
                Tshirt: Tshirt,
                stemmi:stemmi
            }
        },
        methods: {
            getRating(voto) {
        return Math.ceil(voto / 2)
      },
        }

    }
</script>

<style lang="scss" scoped>
.bg-shirt{
    background-color: var(--secondaryBlue);
}
.box-image .list .item{
    width: 100%;
    padding: 10px;
    background-color: var(--color-cards);
    border-radius: 6px;
    cursor: pointer;
    transition: all ease 0.4s;
}
.box-image .list .item:hover{
    background-color: var(--colorRed);
}
.voto{
    color: white;
}
.fa-regular{
    color: aqua;
}
</style>