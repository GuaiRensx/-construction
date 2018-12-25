<template>
	<div class="footer">
		<mt-tabbar v-model="selected">
			<mt-tab-item id="全部">
				<img slot="icon" src="../../../build/logo.png"> 全部
			</mt-tab-item>
			<mt-tab-item id="验收中">
				<img slot="icon" src="../../../build/logo.png"> 验收中
			</mt-tab-item>
			<mt-tab-item id="复验中">
				<img slot="icon" src="../../../build/logo.png"> 复验中
			</mt-tab-item>
			<mt-tab-item id="已验收">
				<img slot="icon" src="../../../build/logo.png"> 已验收
			</mt-tab-item>
		</mt-tabbar>
	</div>
</template>

<script>
	import Vue from 'vue'
	import { Tabbar, TabItem } from 'mint-ui';

	Vue.component(Tabbar.name, Tabbar);
	Vue.component(TabItem.name, TabItem);
	export default {
		name: 'footer',
		components: {

		},
		data() {
			return {
				selected: '全部',
//				tabs:[
//					{
//						id:'全部',
//						content:'全部'
//					},
//										{
//						id:'验收中',
//						content:'验收中'
//					},
//										{
//						id:'复验中',
//						content:'复验中'
//					},
//										{
//						id:'已验收',
//						content:'全部'
//					},
//				]
			}
		},
		methods: {

		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
	@import '../../../styles/main.less';
	.footer {
		.h(55);
		position:absolute;
		right:0;
		bottom:0;
		left:0;
	}
</style>