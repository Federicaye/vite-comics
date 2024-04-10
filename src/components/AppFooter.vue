<template>
    <div class="bg">
        <div class="container">
            <div class="list">
                <ul v-for="(link, index) in dcComics" :Key="index" class="dcComics"><a href="">{{ link.name }}</a></ul>
                <ul></ul>
                <ul></ul>
            </div>
        </div>
    </div>
    
</template>

<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            dcComics: [
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

<style lang="scss" scoped>
@import '../assets/style/main.scss';

.bg {
    background-image: url("/footer-bg.jpg");
 
}
.container {
        @include container($container: 1000px);
       
    }
.dcComics {
    @include  text-uppercase($white);
   @extend menu-footer !optional;
}
</style>