<template>
<div>
    <topnav />
    <div class="banner">
        <h1>轮子</h1>
        <h2>一个厉害的UI框架</h2>
        <p class="actions">
            <a>github</a>
            <router-link to='/doc'>开始</router-link>
        </p>
    </div>
</div>
</template>

<script lang="ts">
import topnav from '../components/topnav.vue'
export default {
    components: {
        topnav
    }
}
</script>
