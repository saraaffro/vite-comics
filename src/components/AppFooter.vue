<script>
export default {
    name: "AppFooter",
    data() {
        return {
            features: [
                {
                    text: "DIGITAL COMICS",
                    image: "../../public/img/buy-comics-digital-comics.png"
                },
                {
                    text: "DC MERCHANDISE",
                    image: "../../public/img/buy-comics-merchandise.png"
                },
                {
                    text: "SUBSCRIPTION",
                    image: "../../public/img/buy-comics-subscriptions.png"
                },
                {
                    text: "COMIC SHOP LOCATION",
                    image: "../../public/img/buy-comics-shop-locator.png"
                },
                {
                    text: "DC POWER VISA",
                    image: "../../public/img/buy-dc-power-visa.svg"
                },
            ]
        }
    }
}
</script>

<template>
    <footer>
        <section class="features">
            <div class="container">
                <div v-for="feat in features" class="feat">
                    <div class="img-container">
                        <img :src="feat.image" :alt="feat.text">
                    </div>
                    <div class="feat-text">
                        {{ feat.text }}
                    </div>
                </div>
            </div>
        </section>
        <section class="site-info">
            <div class="container">
                <div class="col">
                    <h2>DC COMICS</h2>
                    <ul>
                        <li><a href="#">Characters</a></li>
                        <li><a href="#">Comics</a></li>
                        <li><a href="#">Movies</a></li>
                        <li><a href="#">TV</a></li>
                        <li><a href="#">Games</a></li>
                        <li><a href="#">Videos</a></li>
                        <li><a href="#">News</a></li>
                    </ul>

                    <h2>SHOP</h2>
                    <ul>
                        <li><a href="#">Shop DC</a></li>
                        <li><a href="#">Shop DC Collectibles</a></li>
                    </ul>
                </div>

                <div class="col">
                    <h2>DC</h2>
                    <ul>
                        <li><a href="#">Terms Of Use</a></li>
                        <li><a href="#">Privacy policy (New)</a></li>
                        <li><a href="#">Ad Choices</a></li>
                        <li><a href="#">Advertising</a></li>
                        <li><a href="#">Jobs</a></li>
                        <li><a href="#">Subscriptors</a></li>
                        <li><a href="#">Talent Workshops</a></li>
                        <li><a href="#">CPSC Certificates</a></li>
                        <li><a href="#">Rating</a></li>
                        <li><a href="#">Shop Help</a></li>
                        <li><a href="#">Contact Us</a></li>
                    </ul>
                </div>

                <div class="col">
                    <h2>SITES</h2>
                    <ul>
                        <li><a href="#">DC</a></li>
                        <li><a href="#">MAD Magazine</a></li>
                        <li><a href="#">DC Kids</a></li>
                        <li><a href="#">DC Universe</a></li>
                        <li><a href="#">DC Power Visa</a></li>
                    </ul>
                </div>
            </div>
        </section>
        <section class="info-social">
            <div class="container">
                <a class="button" href="#">SIGN-UP NOW!</a>
                <ul>
                    <li>
                        <h2>FOLLOW US</h2>
                    </li>
                    <li><a href="#">
                            <img src="../../public/img/footer-facebook.png" alt="facebook">
                        </a></li>
                    <li><a href="#">
                            <img src="../../public/img/footer-twitter.png" alt="twitter">
                        </a></li>
                    <li><a href="#">
                            <img src="../../public/img/footer-youtube.png" alt="youtube">
                        </a></li>
                    <li><a href="#">
                            <img src="../../public/img/footer-pinterest.png" alt="pinterest">
                        </a></li>
                    <li><a href="#">
                            <img src="../../public/img/footer-periscope.png" alt="periscope">
                        </a></li>
                </ul>
            </div>
        </section>
    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/general.scss' as *;
@use '../styles/partials/variables' as *;

footer {
    .features {
        background-color: $main-color;
        color: white;


        .container {
            width: 55%;
            margin: 0 auto;
            @include flex;
            flex-wrap: wrap
        }

        .feat {
            @include flex;
            flex-basis: 19%;
            padding: 40px 20px;
        }

        .img-container {
            width: 40px;

            img {
                width: 100%;
            }
        }

        .feat-text {
            padding-left: 10px;
            font-size: 11px;
        }
    }

    .site-info {
        min-height: 100px;
        background-image: url("../../public/img/footer-bg.jpg");
        background-size: cover;

        .container {
            display: flex;
            justify-content: flex-start;
            padding: 40px 0;
            background-image: url(../../public/img/dc-logo-bg.png);
            background-position: right;
            background-repeat: no-repeat;
        }

        .col {
            color: white;
            margin-right: 20px;

            h2 {
                margin: 5px 0;
                font-size: 18px;
            }

            li {

                a {
                    color: #5b6263;
                    font-size: 12px;
                }
            }
        }
    }

    .info-social {
        background-color: #303030;
        padding: 30px 0;

        .container {
            @include flex;

            .button {
                color: white;
                text-decoration: none;
                padding: 10px;
                font-size: 18px;
                border: 2px solid $main-color;
            }

            h2 {
                color: $main-color;
            }

            ul {
                @include flex;

                li {
                    margin: 0 10px;
                }
            }
        }
    }
}
</style>