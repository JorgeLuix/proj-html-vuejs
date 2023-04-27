<template>
    <div>
        <CollectionMain/>
    </div>
    <div>
        <SquadPlayers/>
        <LiveStream/>
        <ExploreProducts/>
    </div>
</template>

<script>
import CollectionMain from '../components/CollectionMain.vue';
import SquadPlayers from '../components/SquadPlayers.vue';
import LiveStream from '../components/LiveStream.vue';
import ExploreProducts from '../components/ExploreProducts.vue';

    export default {
        components: { CollectionMain, SquadPlayers, LiveStream, ExploreProducts },
    
    };
</script>

<style lang="scss" scoped>

</style>