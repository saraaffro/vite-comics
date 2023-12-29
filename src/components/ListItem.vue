<script>
export default {
    name: "ListItem",
    props: {
        items: Object,
    }
}
</script>

<template>
    <div class="thumb">
        <div class="img-thumb-container">
            <img :src="items.thumb" :alt="items.series">
        </div>
        <div class="thumb-title">
            {{ items.series }}
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/general.scss' as *;
@use '../styles/partials/variables' as *;

.thumb {
    flex-basis: 9vw;
    height: 9vw;
    color: white;
    overflow: hidden;
    margin-bottom: 30px;
    position: relative;


    .img-thumb-container {
        width: 100%;
        position: relative;
        padding-bottom: 100%;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            position: absolute;
            top: 0;
            left: 0;
        }
    }

    .thumb-title {
        position: absolute;
        bottom: 0;
        left: 0;
    }
}
</style>