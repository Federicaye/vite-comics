<template>
    <div :class="type"  @mouseover="$emit('highlight')">
        <div class="coverComic"> <img :src="img" :alt="title">
            <h5> <a href=""> {{ title }} </a></h5>
            <p>{{ price }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AppCard',
    props: ['price', 'title', 'type', 'img', 'mouseover']
}
</script>

<style lang="scss" scoped>
.coverComic {
    width: 200px;
    height: 300px;
}

img {
    width: 100%;
    height: 100%;
    object-fit: cover;

}
</style>