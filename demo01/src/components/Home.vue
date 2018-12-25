<template>
	<div class="home">
		<Top></Top>
		<Banner></Banner>
		<Footer></Footer>
		<!--<PageTabbar></PageTabbar>-->
	</div>
</template>

<script>
	import Top from './commons/Top'
	import Banner from './commons/Banner'
	import Footer from './commons/Footer'
//import PageTabbar from './commons/PageTabbar'
	export default {
		name: 'home',
		components: {
			Top,
			Banner,
			Footer
		},
		data() {
			return {
				msg: 'i am home'
			}
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
	@import '../../styles/main.less';
	.home {
		height: 100%;
	}
</style>