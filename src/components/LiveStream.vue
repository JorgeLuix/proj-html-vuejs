
<template>
    <div class="bg-stream p-5">
        <div class="text-center">
            <h6 class="text-uppercase text-danger">our latest videos</h6>
            <h1 class="text-uppercase text-white py-3">check our live streaming</h1>
        </div>
        <div class="streaming container">
            <div class="streaming-card"
                v-for="stream in streaming"
                :key="stream.title"
                :style="{backgroundImage: `url(${stream.img})`}">
                <div>
                    <button type="button" class="btn rounded-0 btn-danger 
                                text-uppercase text-white"> join community
                        <i class="fa-solid fa-circle-chevron-right"></i>
                    </button>
                    <p class="text-white">{{stream.title}}</p>
                </div>
                <div class="play-overlay"></div>
                <div class="play">
                    <i class="fa-solid fa-circle-play"></i>
                </div>
            </div>
        </div>
    </div>
  </template>

<script>
import { streaming } from '../data/data.js';
    export default {
        data(){
            return{
                streaming: streaming
            }
        }
    }
</script>

<style scoped>
.bg-stream{
    background-image: url(../assets/imgs/bg-3.jpg);
}
.streaming {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
.streaming-card {
  height: 300px;
  width: 400px;
  margin: 0.8rem;
  background-size: cover;
  background-position: center;
  display: flex;
  flex-direction: column-reverse;
  padding: 10px;
  position: relative;
}
.play-overlay {
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  opacity: 0;
  transition: opacity 0.3s ease-in-out;
}
.play-overlay:hover {
  opacity: 1;
}
.play{
    position: absolute;
    font-size: 2rem;
    top: 50%;
    left: 50%;
    padding: 18px;
    background-color: #a5a5a4;
    height: 70px;
    width: 70px;
    border-radius: 50%;
    opacity: 1;
    transition: all ease 0.4s;
    transform: translate(-50%, -50%) scale(1);
    color: white;
}
.streaming-card:hover .play{
    cursor: pointer;
    color: red;
}
.play:hover {
  cursor: pointer;
}
.play:hover i {
  transform: scale(1.4);
}

</style>