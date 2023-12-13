<script>
import { library } from '@fortawesome/fontawesome-svg-core'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'



export default {
    components: {
        FontAwesomeIcon
    },
    data() {
        return {}
    },
    methods: {},
    mounted: function () {

    }
}
</script>

<template>
    <section class="jumbo">
        <div class="container">
            <div>
                <h1>Barber Shop</h1>
                <div class="hr"></div>
                <p>The Pinnacle of Male Grooming</p>
                <a class="button" href="#"><span>LEARN MORE</span></a>
            </div>
            <div>
                <img src="../assets/images/avadabarbers_hero_focalmirror-600x825.png" alt="">
            </div>
        </div>
    </section>

    <section class="intro">
        <h2>AWARD WINNING</h2>
        <h1>Pro Barbers</h1>
        <a class="button" href="#"><span>MEET YOUR NEW BARBER</span></a>
        <img src="../assets/triangle.svg">
    </section>

    <section class="services">
        <h2>MENS GROOMING</h2>
        <h1>Services</h1>
        <div class="container">
            <div class="col-left">
                <img src="../assets/images/avadabarbers-trimcut-icon-before.png" alt="">
                <h1>Trim & Cut</h1>
                <p>Avada Barbers are experts in the lickety split trim and hair cut.</p>
                <p>Quick but careful and ridiculously good looking.</p>
            </div>
            <div class="col-center">
                <img src="../assets/images/avadabarbers-washndry-icon.png" alt="">
                <h1>Wash & Dry</h1>
                <p>Take a seat in our fine leather chairs, lean back and let us lather you a fresh head in a luxurious
                    fashion.</p>
            </div>
            <div class="col-right">
                <img src="../assets/images/avadabarbers-beardtrim-icon.png" alt="">
                <h1>Beard Tidy</h1>
                <p>Tame the tangles and untidy facial hairs like a gentleman with our Beard Tidy services from Avada
                    Barbers.</p>
            </div>
        </div>
        <a class="button" href="#"><span>READ ABOUT OUR SERVICES</span></a>
        <img class="triangle" src="../assets/triangle.svg">
    </section>

    <section class="products">
        <h2>WE HAVE YOU COVERED</h2>
        <h1>Avada Grooming Products</h1>
        <div class="container">
            <div>
                <img src="../assets/images/brush_dark-200x200.png" alt="">
                <a href="#">
                    <h1>Brush</h1>
                </a>
                <p>$15.00</p>
            </div>
            <div>
                <img src="../assets/images/scissors-200x200.png" alt="">
                <a href="#">
                    <h1>Scissors</h1>
                </a>
                <p>$85.00</p>
            </div>
            <div>
                <img src="../assets/images/hot_oil_dark-200x200.png" alt="">
                <a href="#">
                    <h1>Hot Oil</h1>
                </a>
                <p>$15.00</p>
            </div>
            <div>
                <img src="../assets/images/straight_razor_dark-200x200.png" alt="">
                <a href="#">
                    <h1>Straight Razor</h1>
                </a>
                <p>$30.00</p>
            </div>
        </div>
        <a class="button" href="#"><span>SHOP OUR PRODUCT RANGE</span></a>
    </section>
</template>

<style scoped lang="scss">
@use "../styles/partials/_variables.scss" as *;


.button {
    @include bottone;
    margin-bottom: 3rem;
}

a {
    text-decoration: none;
}

.jumbo {
    height: 120vh;
    background-image: url("../assets/images/avadabarbers-homepage-hero-bg.jpg");
    background-repeat: no-repeat;
    background-size: cover;

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: $default_width;
        margin: auto;

        h1 {
            color: $color_default;
            font-family: 'Abril Fatface', serif;
            font-size: 5em;
            margin: 1rem 1rem 1rem 0;
        }

        p {
            color: $color_tertiary;
            font-size: 24px;
            margin: 2rem 1rem 1rem 0;
        }
    }
}

.hr {
    border: 2.5px solid $color_secondary;
    width: 50%
}

.intro {
    background-image: url("../assets/images/avadabarbers-about-introbackground.jpg");
    background-size: cover;
    padding-top: 5rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    h2 {
        color: $color_secondary;
        font-size: 1em;
    }

    h1 {
        color: $color_default;
        font-family: 'Abril Fatface', serif;
        font-size: 4em;
        margin: 1rem 1rem 1rem 0;
    }

    img {
        width: 100%;
    }
}

.services {
    background-color: $color_default;
    padding-top: 3rem;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;

    h2 {
        color: $color_secondary;
        font-size: 16px;
        font-weight: 400;
    }

    h1 {
        color: hsla(0, 0%, 69%, 100%);
        ;
        font-family: 'Abril Fatface', serif;
        font-size: 4em;
        margin: 1rem;
    }

    .triangle {
        width: 100%;
        filter: invert(92%);
    }

    .container {
        display: flex;
        justify-content: space-around;
        align-items: flex-start;
        width: $default_width;
        margin-bottom: 2rem;

        h1 {
            color: $color_secondary;
            font-size: 2em;
        }

        p {
            text-align: center;
            max-width: calc(100vh/3);
            line-height: 1.8;
            font-size: 18px;
            color: $color_tertiary;
        }

        .col-left {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;

            img {
                width: 64px;
            }
        }

        .col-center {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;

            img {
                width: 84px;
            }
        }

        .col-right {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;

            img {
                width: 66px;
            }
        }

    }
}

.products {
    background-image: url("../assets/images/avadabarbers-reviewsbackground.jpg");
    background-size: cover;
    padding-top: 3rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;

    h2 {
        color: $color_secondary;
        font-size: 16px;
        font-weight: 400;
    }

    h1 {
        color: hsla(0, 0%, 69%, 100%);
        ;
        font-family: 'Abril Fatface', serif;
        font-size: 4em;
        margin: 1rem;
    }

    .container {
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
        padding-bottom: 3rem;
        width: $default_width;

        div {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        h1 {
            font-family: 'Abril Fatface', serif;
            font-size: 2em;
            color: $color_secondary;
        }

        p {
            color: $color_secondary;
            font-size: 12px;
        }
    }
}
</style>


