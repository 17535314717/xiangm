<template>
	<div id="head">
		<h1>猫眼电影</h1>
	</div>
</template>

<script>
	export default {
		name: 'Head',
		props: {},
		data() {
			return {};
		},
		components: {},
		mounted() {},
		updated() {},
		methods: {}
	};
</script>

<style scoped>
	#head {
		width: 100%;
		height: 50px;
		color: #fff;
		background: #e54847;
		border-bottom: 1px solid #e54847;
		position: relative;
	}
	
	#head h1 {
		font-size: 18px;
		text-align: center;
		line-height: 50px;
		font-weight: normal;
	}
</style>