<script>
import { library } from '@fortawesome/fontawesome-svg-core'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

import { faCartShopping } from '@fortawesome/free-solid-svg-icons'
import { faBars } from '@fortawesome/free-solid-svg-icons'

library.add(faCartShopping)
library.add(faBars)

export default {
    props: {},
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

<template></template>

<style scoped lang="scss">
@use "../styles/partials/_variables.scss" as *;
</style>


