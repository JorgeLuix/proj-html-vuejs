<template>
    <div>
        <CollectionMain/>
    </div>
    <div>
        <SquadPlayers/>
        <LiveStream/>
        <ExploreProducts/>
        <MostPopular/> 
        <TestimonialPopular/>
    </div>
</template>

<script>
import CollectionMain from '../components/CollectionMain.vue';
import SquadPlayers from '../components/SquadPlayers.vue';
import LiveStream from '../components/LiveStream.vue';
import ExploreProducts from '../components/ExploreProducts.vue';
import MostPopular from '../components/MostPopular.vue';
import TestimonialPopular from './TestimonialPopular.vue';

    export default {
        components: { CollectionMain, SquadPlayers, LiveStream, ExploreProducts, MostPopular, TestimonialPopular },
    
    };
</script>

<style lang="scss" scoped>

</style>