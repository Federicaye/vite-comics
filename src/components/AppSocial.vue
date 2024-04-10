<template>
    <div class="container-social">
        <div class="social">
            <button>sign-up now</button>
            <div>follow us <img v-for="(social, index) in socials" :key="index" :src="social.img" :alt="social"></div>

        </div>
    </div>
</template>

<script>
export default {
    name: 'AppSocial',
    data() {
        return {
            socials: [
                { link: '#', img: '/footer-facebook.png' },
                { link: '#', img: '/footer-periscope.png' },
                { link: '#', img: '/footer-pinterest.png' },
                { link: '#', img: '/footer-twitter.png' },
                { link: '#', img: '/footer-youtube.png' },
            ]
        }
    }
}
</script>

<style lang="scss">
@import '../assets/style/main.scss';
@import '../assets/style/partials/_variables.scss';
.container-social {
    background-color: $grey;
}
.social {
    @include container($container: 1000px);
    @extend %flex-align-center;
    justify-content: space-between;
    height: 100px;
    img {
    padding-left: 10px;
    }

}
</style>