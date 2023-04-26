<template>
    <header class="">
        <div class="container d-flex align-items-center justify-content-between">
        <img src="../assets/imgs/logo.png" alt="logo">
            <ul class="d-flex gap-4 text-uppercase align-items-center">
                <li class="p-3" v-for="item in headerItems" :key="item">
                <a class="text-white" href="#">{{ item }}</a> 
                </li>
            </ul>
            <div>
                <button type="button" class="btn rounded-0 btn-light 
                text-uppercase text-danger m-1">
                <i class="fa-solid fa-user text-danger"></i> Log in</button>
                <button type="button" class="btn rounded-0 btn-danger 
                text-uppercase">
                <i class="fa-solid fa-users"></i> Sign up</button>
            </div>
        </div>
    </header>
    <div class="jumbotron">
        <div class="jumb">
            <h1 class="text-uppercase">Online game</h1>
            <h3 class="text-uppercase">genuine money transaction</h3>
            <p class="text-capitalize ">Assertively Communicate An expanded array of mindshare rather than 
                diverse technologies for magnetic applications eamlessly virtual then conveniently monetize synergistic huaman capital</p>
                <button type="button" class="btn rounded-0 btn-light 
                text-uppercase text-danger fw-bold">
                 join us today <i class="fa-solid fa-circle-play"></i></button>  
        </div>
    </div> 
</template>

<script>
import {headerItems } from '../data/data.js'
    export default {
        name: 'headerItems',
        data(){
            return{
                headerItems: headerItems,
            }
        }
    }
</script>

<style lang="scss" scoped>
    header {
        background-color: var(--colorBlue);
    }
    .jumbotron{
        background-color: var(--colorBlue);
        background-image: url(../assets/imgs/bg.jpg);
        background-size: cover;
        background-repeat: no-repeat;
        color: white;
        width: 100%;
        height: 120vh;
    }
    .jumb{
        width: 500px;
        height: 500px;
        padding-top: 9rem;
        padding-left: 6rem;
        margin-left: 6rem;
        line-height: 1.8;
    }
    .jumb h1{
        font-size: 5rem;
    }
</style>