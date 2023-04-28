<template>
     <!--testimonial popular-->
     <div class="bg-testimonial-popular">
      <div class="text-center pt-5">
            <h6 class="text-uppercase text-danger">our recent news</h6>
            <h1 class="text-uppercase text-white py-3">our most popular blog posts</h1>
      </div>
      <div class="cards container d-flex">
        <div v-for="(post, index) in posts" :key="index" 
        class="card rounded-1 m-2 text-white mb-5">
          <div class="card-head p-3 d-flex justify-content-between">
                <div class="d-flex align-items-center justify-content-between">
                  <img :src="post.imageUser" :alt="post.title" />
                   <div class="flex-column px-3 profilo">
                      <h2>{{ post.title }}</h2>
                      <p>{{ post.type }}</p>
                  </div>
                </div>
            <img class="w-img" :src="post.imgteam" :alt="post.title" />
          </div>
          <hr>
          <div class="card-body">
            <p>{{ post.description }}</p>
                <i class="fa solid fa-star voto" v-for="(n, index) in 5" :key="index" 
                :class="(n <= getRating(post.voto) ? 'voto' : 'fa-regular' )" ></i>
                <span class="card-text">5.28</span>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
import { posts } from '../data/data.js';
    export default {
        data() {
    return {
      posts: posts
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
.bg-testimonial-popular{
  background-image: url(../assets/imgs/bg.png);
  background-color: var(--secondaryBlue);
  background-size: contain;
}
.card{
  background-color: var(--color-cards);
}
.card-head img{
  border-radius: 50%;
}
.w-img{
  width: 10%;
}
.profilo{
  line-height: 0.2;
}
.voto{
    color: rgb(240, 243, 243);
    background-color: aqua;
    padding: 5px;
}
span{
  color: aqua;
  padding-left: 8px;
}
i{
  margin: 2px;
  border-radius: 3px;
  
}
</style>