<script>
export default {
    name: "AppHeader"
}
</script>

<template>
    <header>
        <div class="logo-container">
            <img src="../../public/img/dc-logo.png" alt="logo">
        </div>
        <ul>
            <li><a href="#">testo</a></li>
            <li><a href="#">testo</a></li>
            <li><a href="#">testo</a></li>
            <li><a href="#">testo</a></li>
            <li><a href="#">testo</a></li>
            <li><a href="#">testo</a></li>
            <li><a href="#">testo</a></li>
            <li><a href="#">testo</a></li>
            <li><a href="#">testo</a></li>
            <li><a href="#">testo</a></li>
        </ul>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/general.scss' as *;
@use '../styles/partials/variables' as *;

header {
    @include flex;
    height: 100px;
    width: 100%;

    .logo-container {
        max-width: 80px;

        img {
            max-width: 100%;
        }
    }

    ul {
        list-style-type: none;
        @include flex;


        li a {
            color: black;
            text-decoration: none;
            padding: 20px 10px;

            &:hover,
            &.active {
                color: $main-color;
            }

            &.active {
                border-bottom: 3px solid $main-color;
            }
        }


    }
}
</style>
