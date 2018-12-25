<template>
  <div class="page-tabbar">
    <div class="page-wrap">
      <div class="page-title">Tabbar</div>
      <div>
        <mt-cell class="page-part" title="当前选中" :value="selected" />
      </div>
 
	<!-- tabcontainer -->
      <mt-tab-container class="page-tabbar-container" v-model="selected">
        <mt-tab-container-item id="外卖">
          <mt-cell v-for="n in 10" :title="'餐厅 ' + n" />
        </mt-tab-container-item>
        <mt-tab-container-item id="订单">
          <mt-cell v-for="n in 5" :title="'订单 ' + n" />
        </mt-tab-container-item>
        <mt-tab-container-item id="发现">
          <mt-cell v-for="n in 7" :title="'发现 ' + n" />
        </mt-tab-container-item>
        <mt-tab-container-item id="我的">
          <div class="page-part">
		   <!-- cell -->
            <mt-cell v-for="n in 12" :title="'我的 ' + n" />
          </div>
          <router-link to="/">
		   <!-- button -->
            <mt-button type="danger" size="large">退出</mt-button>
          </router-link>
        </mt-tab-container-item>
      </mt-tab-container>
    </div>
 
    <mt-tabbar v-model="selected" fixed>
      <mt-tab-item id="外卖">
        <img slot="icon" src="../../../build/logo.png">
        外卖
      </mt-tab-item>
      <mt-tab-item id="订单">
        <img slot="icon" src="../../../build/logo.png">
        订单
      </mt-tab-item>
      <mt-tab-item id="发现">
        <img slot="icon" src="../../../build/logo.png">
        发现
      </mt-tab-item>
      <mt-tab-item id="我的">
        <img slot="icon" src="../../../build/logo.png">
        我的
      </mt-tab-item>
    </mt-tabbar>
  </div>
</template>
 
<script>
export default {
  name: 'PageTabbar',
  data() {
    return {
      selected: '外卖'
    };
  }
};
</script>
 
<style>
  .page-tabbar {
    overflow: hidden;
    height: 100vh;
  }
 
  .page-wrap {
    overflow: auto;
    height: 100%;
    padding-bottom: 100px;
  }
</style>
tabs:[
					{
						id:'全部',
						content:'全部',
						img:'../../../build/logo.png'
					},
										{
						id:'验收中',
						content:'验收中',
						img:'../../../build/logo.png'
					},
										{
						id:'复验中',
						content:'复验中',
						img:'../../../build/logo.png'
					},
										{
						id:'已验收',
						content:'已验收',
						img:'../../../build/logo.png'
					},
				]