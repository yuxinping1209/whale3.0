<template>
	<Button @click="onClick" @focus="onClick" @mouseover="onClick">按钮</Button>
	<Button theme="text" @click="onClick" @focus="onClick" @mouseover="onClick">按钮</Button>
	<Button theme="link" @click="onClick" @focus="onClick" @mouseover="onClick">按钮</Button>
	<Button theme="button" @click="onClick" @focus="onClick" @mouseover="onClick">按钮</Button>
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
			return{onClick}
		}
	}
</script>

<style>
</style>
