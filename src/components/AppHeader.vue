<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    status: false,
                },
                {
                    text: "COMICS",
                    status: true,
                },
                {
                    text: "MOVIES",
                    status: false,
                },
                {
                    text: "TV",
                    status: false,
                },
                {
                    text: "GAMES",
                    status: false,
                },
                {
                    text: "COLLECTIBLES",
                    status: false,
                },
                {
                    text: "VIDEOS",
                    status: false,
                },
                {
                    text: "FANS",
                    status: false,
                },
                {
                    text: "NEWS",
                    status: false,
                },
                {
                    text: "SHOP",
                    status: false,
                },
            ]
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <div class="logo-container">
                <img src="../../public/img/dc-logo.png" alt="logo">
            </div>
            <ul>
                <li v-for="(link, i) in  links" :key="i"><a :class="link.status ? 'active' : ''" href="#">{{ link.text
                }}</a></li>
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
    position: fixed;
    top: 0;
    left: 0;
    z-index: 500;
    background-color: white;

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
                padding: 31px 7px;
                font-size: 12px;

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
