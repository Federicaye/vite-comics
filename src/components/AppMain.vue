<template>
    <div class="cards">
        <div v-for="(item, index) in comics" :key="index" class="card">
            <AppCard :price="item.price" :title="item.series" :type="item.type" :img="item.thumb" />
        </div>
    </div>
</template>

<script>
import { comics } from '../data/store.js';
import AppCard from './AppCard.vue';
export default {
    name: 'AppMain',
    components: {
        AppCard,
    },
    data() {
        return {
            comics,
        }
    }
}
</script>

<style lang="scss">
@import '../assets/style/main.scss';

.cards {
    @extend %flex-align-center;
    background-color: rgb(0, 0, 0);
    flex-wrap: wrap;
    
}

.card {
    width: calc(100% / 6);
}
</style>