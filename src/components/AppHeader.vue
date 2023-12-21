<script>
export default {
    name: "AppHeader"
}
</script>

<template>
    <header>
        <div class="container">
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
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/general.scss' as *;
@use '../styles/partials/variables' as *;

header {
    height: 80px;
    width: 100%;

    .container {
        @include flex;
        height: 100%;

        .logo-container {
            width: 55px;

            img {
                width: 100%;
            }
        }

        ul {
            @include flex;


            li a {
                color: black;
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
}
</style>
