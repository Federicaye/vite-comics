<template>
    <nav class="container">
        <img id="logo" src="/dc-logo.png" alt="">
        <div>
            <ul class="main-menu">
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

#logo {
    width: 70px;
}

.container {
    @include container($container: 1000px);
    @extend %flex-align-center;
    justify-content: space-between;
    
    .main-menu {
        @include text-uppercase($text-uppercase: rgb(0, 0, 0));
        @extend %flex-align-center;
        gap: 20px;
        font-family: "Antonio", sans-serif; ;

    }
}
</style>