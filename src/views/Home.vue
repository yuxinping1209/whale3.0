<template>
	<div>
		<topnav />
		<div class="banner">
			<h1>轮子</h1>
			<!-- <h2>一个厉害的UI框架</h2> -->
			<p class="actions">
				<a>github</a>
				<div>
					<button style="padding:5px 30px;text-decoration: none;background-color: #00aa7f;border:none;border-radius: 5px;">
						<router-link to='/doc'>开始</router-link>
					</button>
				</div>


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
<style lang="scss">
	.banner {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height: 50vh;
	}
</style>
