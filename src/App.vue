<template>
	<router-view></router-view>
</template>

<script>
	import {
		provide,
		ref
	} from 'vue'
	import {
		router
	} from './router'
	export default {
		name: 'App',
		components: {

		},
		setup() {
			const width = document.documentElement.clientWidth
			const asideVisible = ref(width <= 500 ? false : true)
			provide("asideVisible", asideVisible)
			router.afterEach(() => {
				if (width <= 500) {
					asideVisible.value = false
				}
			})
		}
	}
</script>
