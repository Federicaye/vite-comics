<template>
    <div class="cards">
        <div class="shop">
            <div v-for="(item, index) in comics" :key="index" class="cardComic" :class="{ 'borderWhite': item.mouseover }">
                <AppCard :price="item.price" :title="item.series" :type="item.type" :img="item.thumb"
                    @highlight="highlighting(index)" />
            </div>
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
    },
    methods: {
        highlighting(index) {
            this.item[index].mouseover = !this.item[index].mouseover
        }
    }
}
</script>

<style lang="scss">
@import '../assets/style/main.scss';

.cards {

    background-color: rgb(0, 0, 0);
}

.shop {
    @include container($container: 1200px);
    @extend %flex-align-center;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 10px;
}

.cardComic {
    width: calc(100% / 6);
    color: white;
    height: 400px;
}

.borderWhite {
    border: 5px, solid, white;


}
</style>