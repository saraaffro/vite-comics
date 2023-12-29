<script>
export default {
    name: "ListItem",
    props: {
        items: {
            type: Object,
            required: true,
        }
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
    flex-basis: calc(100% / 6);
    color: white;

    .img-thumb-container {
        width: 100%;

        img {
            width: 100%;
        }
    }
}
</style>