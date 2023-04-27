<template>
    <div>
        <CollectionMain/>
    </div>
    <div>
        <SquadPlayers/>
    </div>
</template>

<script>
import CollectionMain from '../components/CollectionMain.vue';
import SquadPlayers from '../components/SquadPlayers.vue';

    export default {
        components: { CollectionMain,SquadPlayers },
    
    };
</script>

<style lang="scss" scoped>

</style>