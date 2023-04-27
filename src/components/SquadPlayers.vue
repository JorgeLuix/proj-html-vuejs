<template>
    <div class="squad-players">
        <div class="text-center">
            <h6 class="text-uppercase text-danger">our team players</h6>
            <h1 class="text-uppercase text-white py-3">meet our squad players</h1>
        </div>
        <div class="card-container">
            <div class="row">
                <div class="col-md-4 col-lg-2" v-for="item in squad" :key="item.title">
                    <div class="cards m-4 mb-3" :style="{ 'background-image': 'url(' + item['imgbg'] + ')', 
                    'background-size': 'cover', 'width': '100%', 'height': '100%' }">
                            <img :src="item.img" :alt="item.title" class="card-img">
                        <div class="card-body text-center text-white">
                            <h5 class="card-title">{{item.title}}</h5>
                            <div class="social d-flex">
                                <img src="../assets/imgs/social-1.png" alt="vi">
                                <img src="../assets/imgs/social-2.png" alt="youtube">
                                <img src="../assets/imgs/social-3.png" alt="twicht">
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!--section join gamer-->
        <div class="play-gamer container">
            <div class="row">
                <div class="col-lg-6 p-5">
                    <div>
                        <h6 class="text-uppercase text-danger">let's play together</h6>
                        <h1 class="text-uppercase text-white py-3">join gamer esport to become next pro gamer today!</h1>
                        <p class="text-white">Distinctively provide acces mutfuncto users whereas transparent proceses
                             somes ncentivize eficient functionalities rather than an extensile archtectur services and cross</p>
                        <button type="button" class="btn rounded-0 btn-light 
                    text-uppercase text-danger my-5"> join community
                    <i class="fa-solid fa-circle-chevron-right"></i>
                        </button>
                     </div>
                </div>
                <div class="col-lg-6 p-5">
                    <img class="w-75" src="../assets/imgs/01 (1).png" alt="">
                </div>
            </div>
        </div>
    </div>
  </template>
<script>
import { squad } from '../data/data.js'
export default {
    data(){
        return{
            squad: squad,
        }
    }
  }
</script>
<style scoped>
h1{
    font-size: 3rem;
}
.squad-players{
    background-color: var(--secondaryBlue);
}
.card-container {
    width: 100%;
  display: flex;
  justify-content: center;
}
.cards {
  /*margin: 10px;*/
  margin-bottom: 10px;
  padding: 3rem;

}

.cards-img {
 width: 50%;
 display: flex;
 flex-direction: column;
 align-content: center;
 justify-content: center;

}
.social img{
    padding: 8px;
}
.card-body {
  padding: 10px;
}
.play-gamer{
    background-image: url(../assets/imgs/bgGamer.jpg);
    background-repeat: no-repeat;
    margin-top: 8rem;
    
}
</style>