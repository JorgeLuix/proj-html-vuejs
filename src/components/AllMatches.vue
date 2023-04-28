<template>
    <main class="">
        <div class="d-flex p-5 container justify-content-center">
            <div class=" text-center">
                <h2 class="text-white">Upcoming matches</h2>
                    <div v-for="(match, index) in group" :key="`upcoming-${index}`" 
                        class="card m-3 rounded-0">
                        <section class="card-header rounded-0 bg-danger text-white d-flex justify-content-between">
                            <div class="d-flex">
                                <p>2 group</p>
                                <p cl>32 players</p>
                            </div>
                                <span>Price Pool: $3200</span>
                        </section>
                        <div class="card-body d-flex justify-content-between">       
                            <img :src="upcomingmatches[match[0]]" class="">
                            <div class="mx-5">
                                <div v-for="(event, index) in datamatch" :key="index">
                                
                                </div>
                                <p>{{ getCurrentDateTime() }}</p>
                                <img src="../assets/imgs/social-1.png" alt="">
                                <img class="mx-2" src="../assets/imgs/social-2.png" alt="">
                                <img src="../assets/imgs/social-3.png" alt="">
                            </div>
                            <img :src="upcomingmatches[match[1]]" class="img-fluid my-3">
                        </div> 
                    </div>
            </div>
            <div class=" text-center">
                <h2 class="text-white">Previous matches</h2>
                <div class="">
                    <div v-for="(match, index) in grouptwo" :key="`previous-${index}`"
                    class="card m-3 rounded-0">
                        <section class="card-header rounded-0 bg-danger text-white d-flex justify-content-between">
                            <div class="d-flex">
                                <p>2 group</p>
                                <p cl>32 players</p>
                            </div>
                            <span>Price Pool: $3200</span>
                        </section>
                            <div class="card-body d-flex">
                                <img  :src="previousmatches[match[0]]" class="img-fluid my-3">
                                <div class="mx-5">
                                    <h6 class="text-center">8:4</h6>
                                    <p>{{ getCurrentDateTime() }}</p>
                                    <img src="../assets/imgs/social-1.png" alt="">
                                    <img class="mx-2" src="../assets/imgs/social-2.png" alt="">
                                    <img src="../assets/imgs/social-3.png" alt="">
                                </div>
                                <img :src="previousmatches[match[1]]" class="img-fluid my-3">
                            </div>
                    </div>
                </div>
            </div>
        <!-- <h2>Current match</h2>
            <div class="card">
            <h3>{{ currentMatch }}</h3>
            </div>-->
        </div>
    </main>
</template>

<script>
import { upcomingmatches } from '../data/data.js';
import { previousmatches } from '../data/data.js';
import { datamatch } from '../data/data.js'
export default {
  name: 'Matches',
  data(){
    return{
        group:[
        [0, 1],
        [2, 3],
        [4, 5]
      ],
      grouptwo: [
        [0, 1],
        [2, 3],
        [4, 5]
      ],
        upcomingmatches: upcomingmatches,
        previousmatches: previousmatches,
        datamatch: datamatch
    }
  },
  methods: {
    getCurrentDateTime() {
      const currentDateTime = new Date();
      return currentDateTime.toLocaleString();
    },
  },
}
</script>

<style>
main{
    background-image: url(../assets/imgs/bgg-1.jpg);
    background-size: contain;
}
.bg-head{
    background-color: var(--colorRed);
}

</style>
