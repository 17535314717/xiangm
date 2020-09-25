<template>
  <div class="top" style="display: block;">
  	<a id="download-header" href="#" style="">
  		<div class="bar">
  			<h1><img class="img noneBg logo" alt="logo" src="../../public/img/mao1.png" width="42" height="42"></h1>
  			<div class="desc">
  				<div class="appName">猫眼</div>
  				<div class="appDesc">在线选座，热门影讯，爱上看电影</div>
  			</div>
  			<div class="btnApp" :style="{'background': bgColor}">打开App</div>
  		</div>
  	</a>
  </div>
</template>

<script>
export default {
  name: 'top',
  props: {
	  bgColor:{
		  type:String,
		  default:'#ef4238'
	  }
  },
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
.bar {
		position: relative;
		height: 63px;
		background-color: #fff;
		border-bottom: 1px solid #e6e6e6;
	}

	.bar h1 {
		display: inline;
	}

	h1 {
		font-size: 2em;
		margin: .67em 0;
		margin-block-start: 0.67em;
		margin-block-end: 0.67em;
		margin-inline-start: 0px;
		margin-inline-end: 0px;
		font-weight: bold;
	}

	.bar img{
		position: absolute;
		left: 15px;
		top: 11px;
		width: 44px;
		height: 44px;
	}

	img {
		display: block;
	}

	.bar .desc {
		position: absolute;
		left: 66px;
		top: 13px;
	}

	.bar .desc .appName {
		font-size: 17px;
		color: #222;
		line-height: 23px;
	}

	.bar .desc .appDesc {
		font-size: 12px;
		color: #999;
	}

	.bar .btnApp {
		position: absolute;
		right: 15px;
		top: 17px;
		width: 68px;
		height: 30px;
		line-height: 30px;
		text-align: center; 
		border-radius: 3px;
		font-size: 13px;
		color: #fff;
	}
</style>
