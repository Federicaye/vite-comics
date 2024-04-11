<template>
    <div :class="type">
        <img :src="img" :alt="title">
        <h5> <a href=""> {{ title }} </a></h5>
        <p>{{ price }}</p>
    </div>
</template>

<script>
export default {
    name: 'AppCard',
    props: ['price', 'title', 'type', 'img']
}
</script>

<style lang="scss" scoped>
img {
    width: 100%;
}
</style>