<template>
	
	<dir>
		<Button>按钮</Button>
		<Button theme="button">按钮</Button>
		<Button theme="text">按钮</Button>
		<Button theme="link">按钮</Button>
	</dir>
	<dir>
		<Button size="normal">按钮</Button>
		<Button size="big">按钮</Button>
		<Button size="small">按钮</Button>
	</dir>

</template>

<script lang="ts">
	import Button from '../lib/Button.vue'
	export default {
		components: {
			Button
		},
		setup() {
			const onClick = () => {
				console.log('hi')
			}
			return {
				onClick
			}
		}
	}
</script>

<style>
</style>
