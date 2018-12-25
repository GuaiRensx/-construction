<template>
	<div class="banner">
		<mt-swipe :auto="4000">
			<mt-swipe-item><img src="../../assets/1.jpg"/></mt-swipe-item>
			<mt-swipe-item><img src="../../assets/2.jpeg"/></mt-swipe-item>
			<mt-swipe-item><img src="../../assets/3.jpg"/></mt-swipe-item>
		</mt-swipe>
	</div>
</template>

<script>
	import Vue from 'vue'
	import { Swipe, SwipeItem } from 'mint-ui';

	Vue.component(Swipe.name, Swipe);
	Vue.component(SwipeItem.name, SwipeItem);
	export default {
		name: 'banner',
		components: {},
		data() {
			return {
				msg: 'i am banner',
				show: false
			}
		},
		methods: {

		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
	@import '../../../styles/main.less';
	.banner {
		/*.margin-top(40);*/
		background:pink;
		.h(150);
		width: 100%;
		img{
			width: 100%;
			height: 100%;
		}
	}
</style>