<template>
<router-view></router-view>
</template>

<script>
import {
    provide,
    ref
} from 'vue'

export default {
    name: 'App',
    components: {

    },
    setup() {
        const asideVisible = ref(true)
        provide("asideVisible", asideVisible)
    }
}
</script>
