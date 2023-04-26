<template>
    <div class="main-collection">
        <div class="container text-center p-5">
            <div>
                <h6 class="text-uppercase">today's</h6>
                <h1 class="text-uppercase text-white">our game collection</h1>
            </div>
            <div class=" container d-flex justify-content-between">
                <div class="row card card-bg p-5" v-for="(card, index) in cards" :key="index">
                    <div class=" col d-flex align-items-center">
                        <img  :src="teams[card[0]]">
                        <img class="px-2" src="../assets/imgs/vs.png" alt="">
                        <img :src="teams[card[1]]">
                    </div>
                </div>
            </div>
            <button type="button" class="btn rounded-0 btn-light 
                    text-uppercase text-danger my-5"> browse all games
                    <i class="fa-solid fa-circle-chevron-right"></i></button>
            <hr class="container pt-5">
        </div>
    </div>
    
    <div>2</div>
</template>

<script>
import { teams } from '../data/data.js';

    export default {
     
    data(){
        return{
            cards:[
        [0, 1],
        [2, 3],
        [4, 5]
      ],
      teams: teams
    };
}
    };
</script>

<style lang="scss" scoped>
.main-collection {
    background-color: var(--secondaryBlue);
}
h6{
    color: var(--colorRed);
}
.card-bg{
    background-color: rgb(35, 35, 93);
}
hr{
    color: gray;
}
</style>