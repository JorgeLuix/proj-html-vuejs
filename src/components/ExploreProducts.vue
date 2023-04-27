<template>
    <div class="bg-shirt p-5">
        <div class="text-center">
            <h6 class="text-uppercase text-danger">gamer t-shirt's</h6>
            <h1 class="text-uppercase text-white py-3">explore our products</h1>
        </div>
        <div class="box-image container">
            <div class="image-col list d-flex ">
                <div class="card item m-2" v-for="(shirt, index) in Tshirt" :key="index">
                    <img :src="shirt.img" alt="">
                    <div class="text-center text-white">
                        <p class="">{{ shirt.title }}</p>
                        <p>{{ shirt.prezzo }}</p>
                        <span class="card-text"></span>
                    <i class="fa solid fa-star voto" v-for="(n, index) in 5" :key="index" 
                    :class="(n <= getRating(shirt.voto) ? 'voto' : 'fa-regular' )" ></i>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { Tshirt } from '../data/data.js';
    export default {
        data(){
            return{
                Tshirt: Tshirt
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