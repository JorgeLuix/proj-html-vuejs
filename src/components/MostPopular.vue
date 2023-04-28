<template>
    <div class="bg-popular">
            <div class="text-center pt-5">
                <h6 class="text-uppercase text-danger">our recent news</h6>
                <h1 class="text-uppercase text-white py-3">our most popular blog posts</h1>
            </div>
      <div class="box-image container">
         <div class="list d-flex">
            <div class="card rounded-0 item m-2 mb-5" 
                 v-for="(item, index) in popular" :key="index">
                  <img :src="item.img" alt="">
                  <div class="text-white py-3">
                      <h3>{{ item.title }}</h3>
                    <div class="d-flex px-3">
                      <p class="pe-3 text-capitalize jc-shadow"> {{ item.user }}</p>
                      <p>{{ getCurrentDate() }}</p>
                    </div>
                        <p> {{ item.description }}</p>
                        <button type="button" class="btn rounded-1 btn-danger 
                      text-uppercase text-white"> read more
                      <i class="fa-solid fa-arrow-right ps-2"></i>
                        </button>
                </div>
            </div>
        </div>
      </div>
    </div>
  </template>

<script>
import { popular } from '../data/data.js';
export default {
  data() {
    return {
      popular: popular
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
    }
  }
}
</script>

<style lang="scss" scoped>
.bg-popular{
    background-image: url(../assets/imgs/bgg-2.jpg);
    background-size: contain;
}
.box-image .list .item{
    width: 100%;
    padding: 10px;
    background-color: var(--color-cards);
    border-radius: 6px;
    cursor: pointer;
    transition: all ease 0.4s;
}
.jc-shadow{
  box-shadow: rgb(235, 7, 7) 0px 25px 20px -20px;
}
</style>