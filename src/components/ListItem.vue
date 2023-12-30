<script>
export default {
    name: "ListItem",
    props: {
        items: Object,
    }
}
</script>

<template>
    <a href="#">
        <div class="thumb">
            <div class="img-thumb-container">
                <img :src="items.thumb" :alt="items.series">
            </div>
            <div class="thumb-title">
                {{ items.series }}
            </div>
        </div>
    </a>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/general.scss' as *;
@use '../styles/partials/variables' as *;

.thumb {
    width: 9vw;
    height: 9vw;
    color: white;
    margin-bottom: 70px;

    .img-thumb-container {
        height: 100%;

        img {
            width: 100%;
            height: 100%;
        }
    }

    .thumb-title {
        margin-top: 15px;
        font-size: 10px;
        text-transform: uppercase;
    }
}
</style>