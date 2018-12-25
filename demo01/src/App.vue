<template>
  <div id="app">
    <Home/>
  </div>
</template>

<script>
import Home from './components/Home'

export default {
  name: 'App',
  components: {
    Home
  }
}
</script>

<style lang="less" scoped>
@import '../styles/main.less';
#app{
	height: 100%;
	font-family: 'Avenir', Helvetica, Arial, sans-serif;
 -webkit-font-smoothing: antialiased;
 -moz-osx-font-smoothing: grayscale;
	.fs(16);
 color: #2c3e50;
}
</style>
