<template>
<div class="layout">
    <topnav class="nav" />
    <div class="content">

        <aside v-if="asideVisible">
            <ol>
                <h2>组件列表</h2>
                <li><router-link to="/doc/switch">switch</router-link></li>
                <li><router-link to="/doc/button">button</router-link></li>
                <li><router-link to="/doc/dialog">dialog</router-link></li>
                <li><router-link to="/doc/switch">switch</router-link></li>
                <li><router-link to="/doc/switch">switch</router-link></li>
                <li><router-link to="/doc/switch">switch</router-link></li>
                <!-- <router-link>button</router-link>
                <router-link>dialog</router-link>
                <router-link>tab</router-link>
                <router-link>其他</router-link> -->
            </ol>
        </aside>
        <main><router-view/></main>
    </div>
</div>
</template>

<script lang="ts">
import {
    inject,
    Ref
} from 'vue'
import topnav from '../components/topnav.vue'
export default {
    components: {
        topnav
    },
    setup() {
        const asideVisible = inject < Ref < boolean >> ('asideVisible');
        console.log('doc', asideVisible.value)
        return {
            asideVisible
        }
    }

}
</script>

<style lang="scss">
.layout {
    display: flex;
    flex-direction: column;
    height: 100vh;

    >.nav {
        flex-shrink: 0;
    }

    >.content {
        flex-grow: 1;
        padding-top: 60px;
        padding-left: 156px;

        @media (max-width: 500px) {
            padding-left: 0;
        }
    }
}

.content {
    display: flex;

    >aside {
        flex-shrink: 0;
        padding-left: 20px;
    }

    >main {
        flex-grow: 1;
        padding: 16px;
        background: white;
    }
}

aside {
    background: #efefef;
    width: 150px;
    padding: 16px 0;
    position: fixed;
    top: 0;
    left: 0;
    padding-top: 70px;
    height: 100%;

    >ol>h2 {
        margin-bottom: 10px;
        // padding: 0 16px;
    }
	>ol>li{
		list-style: none;
		margin-bottom: 10px;
	}
}
</style>
