<template>
	<div class="topnav">
		<div class="logo" @click="toggleAside">LOGO</div>
		<div class="menu">
			<span style="margin-right:20px;">菜单1</span>
			<span>菜单2</span>
		</div>
	</div>
</template>

<script lang="ts">
	import {
		inject,
		Ref
	} from 'vue';
	export default {
		setup() {

			const asideVisible = inject < Ref < boolean >> ('asideVisible');
			const toggleAside = () => {
				asideVisible.value = !asideVisible.value
			};
			return {
				toggleAside
			}

		}
	}
</script>

<style lang="scss">
	.topnav {
		background: #00aa7f;
		display: flex;
		justify-content: space-between;
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		z-index: 10;

		.logo,
		.menu {
			margin: 20px 40px 20px 40px;

		}

		.logo {
			font-size: 20px;
			font-weight: bold;
			color: #eee;
		}

		.menu {
			font-size: 16px;
			color: #eee;
		}
	}
</style>
