<script>
import { library } from '@fortawesome/fontawesome-svg-core'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

import { faCartShopping } from '@fortawesome/free-solid-svg-icons'
import { faBars } from '@fortawesome/free-solid-svg-icons'
import { faXmark } from '@fortawesome/free-solid-svg-icons'

library.add(faCartShopping)
library.add(faBars)
library.add(faXmark)

export default {
    props: {
        menu: Array,
    },
    components: {
        FontAwesomeIcon
    },
    data() {
        return {
            menuToggle: false
        }
    },
    methods: {
        menu_entry_active: function (i) {
            console.log(i)
            if (i == 0) {
                return "active";
            }
        }
    },
    mounted: function () {

    }
}
</script>

<template>
    <header>
        <div class="container">
            <div class="logo">
                <img src="../assets/images/avadabarbers-logo-x2-300x104.png" alt="">
            </div>
            <div>
                <FontAwesomeIcon icon="fa-solid fa-cart-shopping" class="icon" />
                <FontAwesomeIcon :icon="['fas', 'bars']" class="icon active" @click="menuToggle = !menuToggle" />
            </div>
        </div>
        <!-- Per far apparire e sparire il menù dell'header -->
        <div v-if="menuToggle" class="navbar">
            <div>
                <FontAwesomeIcon icon="fa-solid fa-xmark" class="icon" @click="menuToggle = !menuToggle" />
            </div>
            <!-- la classe la imposto ad active oppure niente con la funzione menu_entry_active() -->
            <a v-for="(elemento, indice) in  menu " :href="elemento.link">
                <p :class="menu_entry_active(indice)">{{ elemento.title }}</p>
            </a>
        </div>
    </header>
</template>

<style scoped lang="scss">
@use "../styles/partials/_variables.scss" as *;

/// definisco lo stile del menù

.navbar {
    position: absolute;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
    padding: 7rem;
    background-color: $background_default;

    a {
        color: $color_default;
        text-decoration: none;

        p {
            font-size: 1.5em;
            font-weight: 400;

        }

        .active,
        p:hover {
            color: $color_secondary
        }
    }

    div {
        position: absolute;
        top: 1rem;
        right: 16px;
    }
}

.container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    width: 80%;
    margin: auto;

}

header {
    background-color: $background_default;
    padding: 1rem;
    position: relative;
}

.logo img {
    width: 192px;
    height: 70px;

}

.icon {
    margin-right: 1rem;
    color: $color_default;
    font-size: 1.5em;

    :hover {
        color: $color_secondary;
    }
}

.active {
    color: $color_secondary
}
</style>


