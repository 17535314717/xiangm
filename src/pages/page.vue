<template>

<router-link to="/cinema">
	<div class="cinema_menu">
		<div class="city_switch">
			<span>全城</span><i class="iconfont icon-lower-triangle"></i>
		</div>
		<div class="brand_swtich">
			<span>品牌</span> <i class="iconfont icon-lower-triangle"></i>
		</div>
		<div class="feature_switch">
			<span>特色</span> <i class="iconfont icon-lower-triangle"></i>
		</div>
	</div>
	<div class="page region">
		<div id="regionTab">
			<ul class="tab">
				<li class="item chosen" data-type="region" data-subnav="#district">商区</li>
				<li class="item" data-type="region" data-subnav="#subway">地铁站</li>
			</ul>
		</div>
		<div id="regioNlist" style="height: 402.64px;">
			<div id="regionSidenav">
				<div id="district">

					<div class="district-li item chosen" data-type="district" data-id="-1">全部(387)</div>

					<div class="district-li item" data-type="district" data-id="5">浦东新区(73)</div>

					<div class="district-li item" data-type="district" data-id="12">闵行区(58)</div>

					<div class="district-li item" data-type="district" data-id="13">宝山区(37)</div>

					<div class="district-li item" data-type="district" data-id="4737">松江区(32)</div>

					<div class="district-li item" data-type="district" data-id="4738">嘉定区(29)</div>

					<div class="district-li item" data-type="district" data-id="2">徐汇区(20)</div>

					<div class="district-li item" data-type="district" data-id="7">普陀区(20)</div>

					<div class="district-li item" data-type="district" data-id="10">杨浦区(18)</div>

					<div class="district-li item" data-type="district" data-id="4739">青浦区(17)</div>

					<div class="district-li item" data-type="district" data-id="6">黄浦区(17)</div>

					<div class="district-li item" data-type="district" data-id="3">静安区(16)</div>

					<div class="district-li item" data-type="district" data-id="664">奉贤区(13)</div>

					<div class="district-li item" data-type="district" data-id="4">长宁区(12)</div>

					<div class="district-li item" data-type="district" data-id="9">虹口区(12)</div>

					<div class="district-li item" data-type="district" data-id="665">金山区(9)</div>

					<div class="district-li item" data-type="district" data-id="666">崇明区(4)</div>

				</div>
				</div>
			<div id="regionListItem">
				<div id="filterList">

					<div class="item chosen" data-type="area" data-id="-1">
						<span class="item-name">全部</span>
						<span class="item-count">73</span>
					</div>

					<div class="item" data-type="area" data-id="31389">
						<span class="item-name">迪士尼</span>
						<span class="item-count">14</span>
					</div>

					<div class="item" data-type="area" data-id="31968">
						<span class="item-name">世博园</span>
						<span class="item-count">12</span>
					</div>

					<div class="item" data-type="area" data-id="282">
						<span class="item-name">张江</span>
						<span class="item-count">7</span>
					</div>

					<div class="item" data-type="area" data-id="275">
						<span class="item-name">陆家嘴</span>
						<span class="item-count">6</span>
					</div>

					<div class="item" data-type="area" data-id="280">
						<span class="item-name">金桥</span>
						<span class="item-count">6</span>
					</div>

					<div class="item" data-type="area" data-id="12141">
						<span class="item-name">滴水湖临港地区</span>
						<span class="item-count">5</span>
					</div>

					<div class="item" data-type="area" data-id="277">
						<span class="item-name">世纪公园</span>
						<span class="item-count">4</span>
					</div>

					<div class="item" data-type="area" data-id="276">
						<span class="item-name">八佰伴</span>
						<span class="item-count">4</span>
					</div>

					<div class="item" data-type="area" data-id="279">
						<span class="item-name">外高桥</span>
						<span class="item-count">3</span>
					</div>

					<div class="item" data-type="area" data-id="9656">
						<span class="item-name">曹路</span>
						<span class="item-count">3</span>
					</div>

					<div class="item" data-type="area" data-id="13320">
						<span class="item-name">浦东机场/机场镇</span>
						<span class="item-count">2</span>
					</div>

					<div class="item" data-type="area" data-id="4748">
						<span class="item-name">南汇/野生动物园</span>
						<span class="item-count">2</span>
					</div>

					<div class="item" data-type="area" data-id="32546">
						<span class="item-name">新国际博览中心</span>
						<span class="item-count">1</span>
					</div>

					<div class="item" data-type="area" data-id="13900">
						<span class="item-name">高行</span>
						<span class="item-count">1</span>
					</div>

					<div class="item" data-type="area" data-id="9657">
						<span class="item-name">北蔡</span>
						<span class="item-count">1</span>
					</div>

					<div class="item" data-type="area" data-id="7472">
						<span class="item-name">金桥商业广场</span>
						<span class="item-count">1</span>
					</div>

					<div class="item" data-type="area" data-id="12127">
						<span class="item-name">航头</span>
						<span class="item-count">1</span>
					</div>

				</div>
				</div>
			<div class="clearfix"></div>
		</div>
	</div>
	
	<div class="blacker"></div>
</router-link>
</template>

<script>
	//import 组件名称 from '组件路径’ 
	export default {
		name: 'Page',
		props: {},
		data() {
			return {

			}
		},
		components: {},
		//生命周期 - 挂载完成
		mounted() {},
		//生命周期 - 更新完成
		updated() {},
		//方法集合
		methods: {},
		//生命周期 - 销毁完成
		destroyed() {

		}
	}
</script>

<style scoped> 
	div{display: block;}
	.cinema_menu {
		width: 100%;
		height: 45px;
		border-bottom: 1px solid #e6e6e6;
		display: flex;
		justify-content: space-around;
		align-items: center;
		background: white;
		position: relative;
	}
	.cinema_menu span,i{color: #CCCCCC;}
	.page {
		background-color: #fff;
		overflow: auto;
		z-index: 999;
		position: relative;
	}
	.page #regionTab{
		height: 44px;
		line-height: 44px;
		text-align: center;
	}
	.page #regionTab ul{
		padding: 0;
		margin: 0;
	}
	
	#regionTab .tab{
		display: flex;
	}
	
	/* 南区  地铁站 */
	.page .region #regionTab ul li {
	    position: relative;
	    display: inline-block;
	    padding: 0 10px;
	    width: 50%;
	    height: 100%;
	    line-height: 44px;
	    text-align: center;
	}
	.page.region #regionTab ul li.chosen {
		color: #f03d37;
		border-bottom: 2px solid #f03d37;
    }
	
	.page .item {
	    font-size: 15px;
	    padding: 0 15px;
	}
	.tab .item {
	    -webkit-box-flex: 1;
	    flex: 1;
	    text-overflow: ellipsis;
	}

	
	.page.region #regioNlist {
	    background: #f5f5f5;
	    height: 380px;
	}
	.page.region #regioNlist #regionSidenav {
	    width: 35%;
	    height: 100%;
	    float: left;
	    overflow: scroll;
	}
	
	.page.region #regioNlist #regionSidenav #district,#subway{
	    min-height: 100%;
	    background: #fff;
	}
	
	.page.region #regioNlist #regionSidenav #district .chosen , #subway .chose{
	    color: #f03d37;
	    background: #f5f5f5;
	}
	
	.district-li {
	    height: 44px;
	    padding-left: 10px;
	    line-height: 44px;
	    font-size: 14px;
	    text-overflow: ellipsis;
	    white-space: nowrap;
	    overflow: hidden;
	}
	
	/* 右侧 */
	.page.region #regioNlist #regionListItem {
	    width: 65%;
	    height: 100%;
	    float: right;
	    overflow: scroll;
	}
	#regionListItem #filterList,#filteRlist {
	    background: #f5f5f5;
	}
	
	#filterList .item,#filteRlist .item {
	    position: relative;
	    height: 45px;
	    line-height: 45px;
	    padding: 0 0 0 25px;
	}
	
	.blacker {
	    z-index: 99;
	    position: fixed;
	    top: 0;
	    left: 0;
	    height: 100%;
	    width: 100%;
	    background: rgba(0,0,0,.3);
	}
</style>
