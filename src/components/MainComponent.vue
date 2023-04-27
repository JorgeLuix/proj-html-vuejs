<template>
    <div>
        <CollectionMain/>
    </div>
    <div>
        <SquadPlayers/>
        <LiveStream/>
    </div>
</template>

<script>
import CollectionMain from '../components/CollectionMain.vue';
import SquadPlayers from '../components/SquadPlayers.vue';
import LiveStream from '../components/LiveStream.vue';


    export default {
        components: { CollectionMain, SquadPlayers, LiveStream },
    
    };
</script>

<style lang="scss" scoped>

</style>