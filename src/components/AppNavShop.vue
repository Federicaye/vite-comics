<template>
    <div class="black">

        <div class="container">
            <ul>
                <li v-for="(link, index) in menu" :key="index">
                    <img :src="link.img" :alt="link.text">{{ link.text }}
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AppNavShop',
    data() {
        return {
            menu: [
                {
                    text: 'digital comics',
                    img: '/buy-comics-digital-comics.png'
                },

                {
                    text: 'digital comics',
                    img: '/buy-comics-shop-locator.png'
                },

                {
                    text: 'digital comics',
                    img: '/buy-comics-subscriptions.png'
                },

                {
                    text: 'digital comics',
                    img: '/buy-dc-power-visa.svg'
                },

                {
                    text: 'digital comics',
                    img: '/buy-comics-digital-comics.png'
                }
            ]
        };
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/main.scss';

.black {
    background-color: #0282f9;
}

.container {
    @include container($container: 1000px);

    ul {
        @extend %flex-align-center;
        list-style: none;
        gap: 20px;
        color: white;
        justify-items: center;
        padding: 30px;

        img {
            width: 40px;
        }

    }
}
</style>