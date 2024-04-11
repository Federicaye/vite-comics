<template>
    <div class="bg">
        <div class="container">
            <div class="list">
               <ul> <li v-for="(link, index) in dcComics" :Key="index" class="dcComics"><a href="">{{ link.name }}</a></li></ul>
               <ul> <li v-for="(link, index) in dcComics" :Key="index" class="dcComics"><a href="">{{ link.name }}</a></li></ul>
               <ul> <li v-for="(link, index) in dcComics" :Key="index" class="dcComics"><a href="">{{ link.name }}</a></li></ul>
            </div>
        </div>
    </div>
    
</template>

<script>
import { footerMenu } from '../data/store.js';
export default {
    name: 'AppFooter',
    data() {
        return {
            dcComics: footerMenu
        }
    }
}
</script>

<style lang="scss">
@import '../assets/style/main.scss';

.bg {
    background-image: url("/footer-bg.jpg");
 
}
.container {
        @include container($container: 1000px);
       
    }

.list {
    color: white;
    display: flex;
}
</style>

