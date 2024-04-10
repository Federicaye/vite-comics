<template>
    <nav class="container">
        <img src="/dc-logo.png" alt="">
        <div>
            <ul>
                <li v-for="(link, index) in menu" :key="index"><a href=""> {{link.name}} </a></li>
            </ul>

        </div>
    </nav>
</template>

<script>
export default {
    name: 'Nav',
    data() {
        return {
            menu: [
                {
                    name: 'Character',
                    url: '#'
                },
                {
                    name: 'Comics',
                    url: '#'
                },
                {
                    name: 'Movies',
                    url: '#'
                },
                {
                    name: 'TV',
                    url: '#'
                },
                {
                    name: 'Games',
                    url: '#'
                },
                {
                    name: 'Collectibles',
                    url: '#'
                },
                {
                    name: 'Videos',
                    url: '#'
                },
                {
                    name: 'Fans',
                    url: '#'
                },
                {
                    name: 'News',
                    url: '#'
                },
                {
                    name: 'Shop',
                    url: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss">
@import '../assets/style/main.scss';

.container {
    @include container($container: 1000px);
    @extend %flex-align-center;
    justify-content: space-between;
    
    ul {
        @extend %flex-align-center;
        list-style: none;
        gap: 20px;

    }
}
</style>