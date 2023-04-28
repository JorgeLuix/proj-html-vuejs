<template>
    <div class="bg-footer">
        <div class="contact text-white">
            <div class="row">
                <div class="col border"></div>
                <div class="col border p-2">
                    <p><i class="fa-solid fa-mobile-screen text-danger fs-1"></i>
                    Phone Number: +526479821456972</p>
                </div>
                <div class="col border d-flex align-items-center">
                    <p><i class="fa-solid fa-envelope-open-text text-danger fs-1"></i>
                    Email: papepipopu@gmail.com</p>
                </div>
                <div class="col border d-flex align-items-center">
                    <p><i class="fa-solid fa-location-dot text-danger fs-1"></i>
                    Address: {{ getCurrentDate() }}</p>
                </div>
                <div class="col border"></div>
            </div>
        </div>
        <div class="form container">
            <div class="row">
                <!--gamer-->
                <div class="col text-white p-3">
                <img class="p-2" src="../assets/imgs/logo.png" alt="">
                <p>È universalmente riconosciuto che un lettore che osserva il layout di una pagina viene distratto dal contenuto testuale se questo è leggibile. 
                    Lo scopo dell’utilizzo del Lorem Ipsum è che offre una normale distribuzione delle lettere (al contrario di quanto avviene se si utilizzano brevi frasi ripetute, ad esempio “testo qui”), apparendo come un normale blocco di testo leggibile.</p>
                    <div class="social py-3">
                        <img src="../assets/imgs/social-1.png" alt="">
                        <img src="../assets/imgs/social-2.png" alt="">
                        <img src="../assets/imgs/social-3.png" alt="">
                    </div>
                <div>
                    <p></p>
                </div>
                </div>
                <!--jackpot-->
                <div class="col text-white p-3">
                    <h1 class="">Top jackpot games</h1>
                    <div class=" d-flex flex-column " v-for="item in jackpot" :key="item.title">
                        <div class="d-flex align-items-center mb-4">
                            <img class="w-img me-3" :src="item.img"/>
                            <div class="text-white">
                                <h5>{{ item.title }}</h5>
                                <p>Poker: {{ item.price }}</p>
                                <i class="fa solid fa-star voto" v-for="(n, index) in 5" :key="index" 
                                :class="(n <= getRating(item.vote) ? 'voto' : 'fa-regular' )" ></i>
                            </div>
                        </div>
                    </div>
                </div>
                <!--newsletter-->
                <div class="col text-white p-3">
                    <h1>our newsletter</h1>
                    <div class="mb-3">
                        <p>Gamer esport organization supported by community leaders</p>
                        <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="Your Name">
                        <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="Your Email">
                    </div>
                    <button type="button" class="btn rounded-0 btn-light 
                    text-uppercase text-danger my-5 btn-shadow"> send massage
                    <i class="fa-solid fa-circle-chevron-right"></i>
            </button>
                </div>
            </div>
        </div>
    </div>
    <div class="footer-copyright d-flex justify-content-center align-items-center ">
        <p><i class="fa-regular fa-copyright"></i>2022 Gamer-eSport And Gameing HTML Template.</p>
        
    </div>
</template>

<script>
import { jackpot } from '../data/data.js'
    export default {
        data(){
            return{
                jackpot: jackpot
            }
        },
        methods: {
    getCurrentDate() {
      const currentDate = new Date().toLocaleDateString('en-US', {
        year: 'numeric',
        month: 'long',
        day: 'numeric'
      });
      return currentDate;
    },
    getRating(voto) {
        return Math.ceil(voto / 2)
      },
  }
    }
</script>

<style lang="scss" scoped>
.bg-footer{
        background-image: url(../assets/imgs/bg-3.jpg);
    }
    .social img {
        padding: 5px;
    }
    .voto{
        color: var(--colorRed);
    }
    input{
        margin-top: 20px;
        border-radius: 0%;
        background-color: var(--color-cards);
        border: none;
    }
.footer-copyright{
    height: 50px;
    background-color: var(--color-cards);
    color: white;
    }
</style>