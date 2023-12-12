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
    </section>
</template>

<style scoped lang="scss">
@use "../styles/partials/_variables.scss" as *;


@mixin bottone {
    padding: 1rem 2rem;
    display: inline-block;
    text-decoration: none;
    border: 2px solid $color_secondary;
    color: $color_secondary;
    font-size: 18px;
    font-weight: 700;
    margin: 2rem 1rem 1rem 0;

    :hover {
        border-color: $color_accent;
        color: $color_accent;
    }
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

        a {
            @include bottone;
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
    padding: 5rem;
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

    a {
        @include bottone;
    }
}
</style>


