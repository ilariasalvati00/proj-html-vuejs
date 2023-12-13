<script>
import { library } from '@fortawesome/fontawesome-svg-core'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

import { faFacebookF } from '@fortawesome/free-brands-svg-icons'
import { faXTwitter } from '@fortawesome/free-brands-svg-icons'
import { faInstagram } from '@fortawesome/free-brands-svg-icons'
import { faYoutube } from '@fortawesome/free-brands-svg-icons'

library.add(faFacebookF);
library.add(faXTwitter);
library.add(faInstagram);
library.add(faYoutube)

export default {
    props: {

    },
    components: {
        FontAwesomeIcon
    },
    data() {
        return {
        }
    },
    methods: {

    },
    mounted: function () {

    }
}
</script>

<template>
    <footer>
        <div class="footer-top">
            <div class="col-left">
                <img src="../assets/images/avadabarbers_footer_shop_image-400x312.png" alt="">
                <a class="button" href="#"><span>SHOP OUR RANGE NOW</span></a>
            </div>
            <div class="col-center">
                <img src="../assets/images/avadabarbers-logo-x2-300x104.png" alt="">
                <div>
                    <p>Avada Barbers</p>
                    <p>123 New York Street</p>
                    <p>New York City</p>
                    <p>info@yourwebsite.com</p>
                    <p>+1 (555) 555-1212</p>
                </div>
                <div>
                    <h2>FOLLOW US</h2>
                    <div class="social">
                        <FontAwesomeIcon icon="fa-brands fa-facebook-f" />
                        <FontAwesomeIcon icon="fa-brands fa-x-twitter" />
                        <FontAwesomeIcon icon="fa-brands fa-instagram" />
                        <FontAwesomeIcon icon="fa-brands fa-youtube" />
                    </div>
                </div>
            </div>
            <div class="col-right">
                <img src="../assets/images/avadabarbers_footer_appointment_image-400x312.png" alt="">
                <a class="button" href="#"><span>BOOK YOU APPOINTMENT</span></a>
            </div>
        </div>
        <div class="footer-bottom">
            <p>© Copyright 2012 - 2023 | Avada Theme by <a href="#">ThemeFusion</a> | All Rights Reserved | Powered by <a
                    href="#">WordPress</a></p>
        </div>
    </footer>
</template>

<style scoped lang="scss">
@use "../styles/partials/_variables.scss" as *;

.footer-top {
    height: $top_footer_height;
    background-color: hsla(0, 0%, 6%, 100%);
    display: flex;
    justify-content: space-around;
    align-items: center;

    .col-left {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .col-center {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-items: space-between;
        color: $color_default;

        img {
            height: $logo-height;
            margin: 1rem;
        }

        div {
            text-align: center;
            padding: 1rem;

            p {
                padding: 0.4rem;
                color: $color_tertiary;
            }

            h2 {
                font-size: 1em;
                color: $color_secondary;
            }
        }

        .social {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 150px;
            color: $color_tertiary;
        }
    }

    .col-right {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .button {
        @include bottone;
        font-size: 14px;
    }
}

.footer-bottom {
    height: $bottom_footer_height;
    background-color: rgba(23, 23, 23, 1);
    display: flex;
    justify-content: center;
    align-items: center;

    p {
        color: $color_tertiary;
        font-size: 13px;
    }

    a {
        text-decoration: none;
        color: $color_secondary;
    }
}
</style>


