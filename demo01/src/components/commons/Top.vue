<template>
	<div class="top">
		<mt-header fixed title="施工文明">
			<router-link to="/" slot="left">
				<mt-button icon="back"></mt-button>
			</router-link>
			<mt-button icon="more" slot="right" @click="moreClick"></mt-button>
		</mt-header>
		<div class="checkedBox" v-if="show">
			<ul>
				<li>安全生产</li>
				<li>文明施工</li>
				<li>施工处罚</li>
			</ul>
		</div>
	</div>
</template>

<script>
	import Vue from 'vue'
	import { Header } from 'mint-ui'
	Vue.component(Header.name, Header);
	export default {
		name: 'top',
		components: {

		},
		data() {
			return {
				msg: '施工文明',
				show: false
			}
		},
		created() {
			document.addEventListener("click", e => {
				//				console.log(e.target);
				if(!this.$el.contains(e.target)) this.show = false;
			});
		},
		destroyed() {
			document.removeEventListener('click')
		},
		methods: {
			moreClick() {
				this.show = true;
			}
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
	@import '../../../styles/main.less';
	.top {
		.h(40);
		.lh(40);
		color: #fff;
		text-align: center;
		.checkedBox {
			z-index: 999;
			.w(100);
			position: fixed;
			background: #26a2ff;
			top: 40px;
			right: 0;
			ul {
				width: 100%;
				border-top: 1px solid #fff;
				border-right: 1px solid #fff;
				li {
					width: 100%;
					.h(40);
					.lh(40);
					border-bottom: 1px solid #fff;
					border-left: 1px solid #fff;
					&:hover {
						color: orange;
					}
				}
			}
		}
	}
</style>