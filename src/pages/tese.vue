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

		<div class="close-tab" style="">
			<div class="tab-content">
				<div class="page special" style="">
					<div id="special-content" style="height: 345.12px;">


						<div class="item-title">特色功能</div>
						<div class="item-list" style="font-size: 14px;">

							<div class="item chosen">全部</div>

							<div class="item">可改签</div>

							<div class="item">可退票</div>

						</div>

						<div class="item-title1">特殊厅</div>
						<div class="item-list">

							<div class="item chosen">全部</div>

							<div class="item">IMAX厅</div>

							<div class="item">CGS中国巨幕厅</div>

							<div class="item">杜比全景声厅</div>

							<div class="item">Dolby Cinema厅</div>

							<div class="item">RealD厅</div>

							<div class="item">RealD 6FL厅</div>

							<div class="item">LUXE巨幕厅</div>

							<div class="item">4DX厅</div>

							<div class="item">DTS:X 临境音厅</div>

							<div class="item">儿童厅</div>

							<div class="item">4K厅</div>

							<div class="item">4D厅</div>

							<div class="item">60帧厅</div>

							<div class="item">120帧/4K厅</div>

							<div class="item">巨幕厅</div>

							<div class="item">CINITY厅</div>

							<div class="item">MX4D厅</div>

						</div>


					</div>
					<div id="special-btn">
						<span class="btn" id="cancel-btn">重置</span>
						<span class="btn" id="confirm-btn">确定</span>
					</div>
				</div>
				</div>
		</div>

		<div class="blacker"></div>
	</router-link>
</template>

<script>
	//import 组件名称 from '组件路径’ 
	export default {
		name: 'Pinp',
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
	div {
		display: block;
	}

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

	.cinema_menu span,
	i {
		color: #CCCCCC;
	}

	/* 品牌下面滚动的 点击出现 */
	.closeTab .page {
		display: block;
	}

	.close-tab {
	    position: relative;
	    width: 100%;
	    background: #fff;
	    z-index: 100;
	    overflow: scroll; 
	}
	.close-tab .tab-content {
	    font-size: 15px;
	}
	.tab-content .page {
	    background-color: #fff;
	    overflow: auto;
	    z-index: 999;
	}
	.close-tab .tab-content .page.special {
	    min-height: 208px;
	}
	.close-tab .tab-content .page {
	    position: relative
	}
	/* 除去按钮以外的 */
	.close-tab .tab-content .page.special #special-content {
	    min-height: 150px;
	    max-height: 270px;
	    overflow: scroll;
	}
	/* 特色功能  特殊厅*/
	.close-tab .tab-content .page.special #special-content .item-title {
	    margin-left: 12px;
	    margin-top: 11px;
	    font-size: 15px;
	}
	/* 特殊功能   下面的小格子 */
	.close-tab .tab-content .page.special #special-content .item-list {
	    margin: 0 12px 12px;
	}
	/* 全部 */
	.close-tab .tab-content .page.special #special-content .item-list .item.chosen {
	    background: #fcf0f0;
	    color: #f03d37;
	    border: 1px solid #f03d37;
	}
	/* 所有格子 */
	.close-tab .tab-content .page.special #special-content .item-list .item {
	    float: left;
	    width: 21.3%;
	    height: 30px;
	    padding: 3px 0;
	    margin-right: 3%;
	    margin-top: 10px;
	    line-height: 30px;
	    overflow: hidden;
	    text-overflow: ellipsis;
	    white-space: nowrap;
	    text-align: center;
	    border: 1px solid #ccc;
	    border-radius: 5px;
	    font-size: 11px;
	}
	.close-tab .tab-content {
	    font-size: 11px;
	}
	.close-tab .tab-content .page.special #special-content .item-title {
		margin-left: 12px;
		margin-top: 11px;
		font-size: 15px;
	}
	.close-tab .tab-content .page.special #special-content .item-title1{
		margin-left: 12px;
		margin-top: 60px;
		font-size: 15px;
	}
	/* 确定按钮 */
	.close-tab .tab-content .page.special #special-btn {
	    height: 60px;
	    width: 100%;
	    border-top: 1px solid #e5e5e5;
	    margin-top: 10px;
	    background: #fafafa;
	}

	.close-tab .tab-content .page.special #special-btn .btn {
	    display: inline-block;
	    height: 34px;
	    width: 21.3%;
	    margin: 13px 11px;
	    border: 1px solid #e5e5e5;
	    border-radius: 6px;
	    text-align: center;
	    line-height: 34px;
	    font-size: 14px;
	}
	.close-tab .tab-content .page.special #special-btn #confirm-btn {
	    float: right;
	    background: #f03d37;
	    border: 1px solid #f03d37;
	    color: #fff;
	}





	.blacker {
		z-index: 99;
		position: fixed;
		top: 0;
		left: 0;
		height: 100%;
		width: 100%;
		background: rgba(0, 0, 0, .3);
	}
</style>
