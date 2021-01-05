<template>
	<div>
		<Button>按钮</Button>
		<Button theme="button">按钮</Button>
		<Button theme="text">按钮</Button>
		<Button theme="link">按钮</Button>
	</div>
	<div>
		<Button size="normal">按钮</Button>
		<Button size="big">按钮</Button>
		<Button size="small">按钮</Button>
	</div>
	<div>
		<Button level="main">主要按钮</Button>
		<Button level="danger">危险按钮</Button>
	</div>
	<div>
		<Button disabled>禁用按钮</Button>
	</div>

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
