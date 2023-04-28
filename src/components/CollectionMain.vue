<template>
    <div class="main-collection">
        <!--section our game-->
        <div class="container text-center p-5">
            <div>
                <h6 class="text-uppercase">today's</h6>
                <h1 class="text-uppercase text-white py-3">our game collection</h1>
            </div>
            <div class=" container d-flex flex-wrap justify-content-center">
                <div class="card card-bg p-3 my-3 mx-3" v-for="(card, index) in cards" :key="index">
                    <div class="d-flex align-items-center">
                        <img  :src="teams[card[0]]" class="img-fluid my-3">
                        <img class="px-2 img-fluid" src="../assets/imgs/vs.png">
                        <img :src="teams[card[1]]" class="img-fluid my-3">
                    </div>
                </div>
            </div>
            <button type="button" class="btn rounded-0 btn-light 
                    text-uppercase text-danger my-5 btn-shadow"> browse all games
                    <i class="fa-solid fa-circle-chevron-right"></i>
            </button>
            <hr class="container pt-5">
        </div>
        <!--section Team esport-->
        <div class="container">
            <div class="row">
                <div class="col-lg-6 p-5">
                    <img class="w-100" src="../assets/imgs/01.png" alt="">
                </div>
                <div class="col-lg-6 p-5">
                    <div>
                        <h6 class="text-uppercase">who we are</h6>
                        <h1 class="text-uppercase text-white py-3">we are professional team esport</h1>
                        <p class="text-white">Distinctively provide acces mutfuncto users whereas transparent proceses
                             somes ncentivize eficient functionalities rather than an extensile archtectur services and cross</p>
                    </div>
                    <div class=" d-flex flex-column " v-for="item in items" :key="item.title">
                        <div class="d-flex align-items-center mb-4">
                            <img class="w-img me-3" :src="item.img"/>
                            <div class="text-white">
                                <h5>{{ item.title }}</h5>
                                <p>{{ item.description }}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { teams } from '../data/data.js';
import { items } from '../data/data.js'

    export default {
     
    data(){
        return{
            cards:[
        [0, 1],
        [2, 3],
        [4, 5]
      ],
      teams: teams,
      items: items
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
    font-size: 1.5rem;
}
h1{
    font-size: 5rem;
}
.card-bg{
    background-color: rgb(35, 35, 93);
}
hr{
    color: gray;
}
.w-img{
    width: 60px;
    height: 60px;
    background-color: var(--colorRed);
    border-radius: 50%;
    padding: 15px;
    margin-right: 20px;
}
</style>