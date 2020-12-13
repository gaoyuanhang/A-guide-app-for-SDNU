<template>
	<view class="contact" >
		<map class="map"  :longitude="longitude" :scale="scale"  :latitude="latitude" :markers="markers" 
		@markertap="openinfo" :show-location="true" show-compass="true"></map>	
			<!-- 悬浮 -->
				<movable-area class="fixed-box">
					<movable-view  class="fixed-button" direction="all" :inertia="true" y="100px">
						<view class="menuBox" >
							<!--这是点击加号图标出现菜单的按钮,可以替换自己页面合适的按钮-->
							<image class="mainMenu" src="../../static/jiahao.jpg" @click="GetLocation()"></image> 
						</view>
					</movable-view>
				</movable-area>

	</view>
</template>

<script>
import helper from '../../common/base.js';
	export default {
		data() {
			return {
				// animationData: {},
				// off:true,
				
				longitude:116.833083,
				latitude:36.544601,
				id:0,
				title: 'map',
				scale:15,
				markers:[
					{
						longitude:116.833683,
						latitude:36.545601,	
						id: 0,
						iconPath:'../../static/1.png',
						width:30,
						height:30,
						callout: {
												content: '图书馆',
												display: 'ALWAYS',//显示方式，可以配置点击或一直显示，BYCLICK点击显示
												padding: '10',//文本边缘留白，文字和边界宽度
												backgroundColor: "#f1f1f1"//背景颜色
											}
					},
					{
						longitude:116.835283,
						latitude:36.542901,	
						id: 1,
						iconPath:'../../static/1.png',
						width:30,
						height:30,
						callout: {
												content: '校医院',
												display: 'ALWAYS',//显示方式，可以配置点击或一直显示，BYCLICK点击显示
												padding: '10',//文本边缘留白，文字和边界宽度
												backgroundColor: "#f1f1f1"//背景颜色
											}
					},
					{
						longitude:116.836483,
						latitude:36.544601,	
						id: 2,
						iconPath:'../../static/1.png',
						width:30,
						height:30,
						callout: {
												content: '第一餐厅',
												display: 'ALWAYS',//显示方式，可以配置点击或一直显示，BYCLICK点击显示
												padding: '10',//文本边缘留白，文字和边界宽度
												backgroundColor: "#f1f1f1"//背景颜色
											}
					},
					{
						longitude:116.834383,
						latitude:36.549901,	
						id: 3,
						iconPath:'../../static/1.png',
						width:30,
						height:30,
						callout: {
												content: '天颐广场',
												display: 'ALWAYS',//显示方式，可以配置点击或一直显示，BYCLICK点击显示
												padding: '10',//文本边缘留白，文字和边界宽度
												backgroundColor: "#f1f1f1"//背景颜色
											}
					},
					{
						longitude:116.830383,
						latitude:36.541401,	
						id: 4,
						iconPath:'../../static/1.png',
						width:30,
						height:30,
						callout: {
												content: '菜鸟驿站',
												display: 'ALWAYS',//显示方式，可以配置点击或一直显示，BYCLICK点击显示
												padding: '10',//文本边缘留白，文字和边界宽度
												backgroundColor: "#f1f1f1"//背景颜色
											}
					},
					{
						longitude:116.830083,
						latitude:36.542401,	
						id: 5,
						iconPath:'../../static/1.png',
						width:30,
						height:30,
						callout: {
												content: '第二餐厅',
												display: 'ALWAYS',//显示方式，可以配置点击或一直显示，BYCLICK点击显示
												padding: '10',//文本边缘留白，文字和边界宽度
												backgroundColor: "#f1f1f1"//背景颜色
											}
					},
					{
						longitude:116.839483,
						latitude:36.549501,	
						id: 6,
						iconPath:'../../static/1.png',
						width:30,
						height:30,
						callout: {
												content: '体育馆',
												display: 'ALWAYS',//显示方式，可以配置点击或一直显示，BYCLICK点击显示
												padding: '10',//文本边缘留白，文字和边界宽度
												backgroundColor: "#f1f1f1"//背景颜色
											}
					},
				]
			}
		},
		methods: {
			GetLocation: function() {
				var that = this;
				 uni.getLocation({
				 	type: 'gcj02',
					success: function(res) {
						res.longitude = 116.830383;
						res.latitude = 36.547901;
						helper.nowlongitude = res.longitude;
						helper.nowlatitude = res.latitude;
						console.log('当前位置的经度：' + helper.nowlongitude);
						console.log('当前位置的纬度：' + helper.nowlatitude);
						uni.openLocation({
						            latitude: helper.nowlatitude,	
						            longitude: helper.nowlongitude,
						            success: function () {
						                console.log('success');
						            },
									});
					}
				 });
			},
			openinfo(e) {
				var id =e.detail.markerId;
				console.log(id);
				if (id==0){
					// #ifdef MP-WEIXIN
					uni.navigateTo({url: '../library/library'});
					// #endif
					// #ifdef H5
					uni.navigateTo({url: '../library/library'});
					// #endif
				}
				if(id==1){
					uni.navigateTo({url: '../hospital/hospital'});
				}
				if(id==2)
				uni.navigateTo({url: '../carteen1/carteen1'});
				if(id==3)
				uni.navigateTo({url: '../square/square'});
				if(id==4)
				uni.navigateTo({url: '../cainiao/cainiao'});
				if(id==5)
				uni.navigateTo({url: '../carteen2/carteen2'});
				if(id==6)
				uni.navigateTo({url: '../gymnasium/gymnasium'});
			},

		},
		
	}
</script>

<style>
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
	}
	.map{
		width: 750rpx;
		height: 1200rpx;
	}
	button::after{
		border:none;
	}
	.menuBox{
		width: 90upx;
		height: 100%;
		z-index: 1;
		position: relative;
		right: -10rpx;
		bottom: 0rpx;
		overflow: hidden;
		border-top-left-radius: 50rpx;
		border-top-right-radius: 50rpx;
		border-bottom-left-radius: 95rpx;
		border-bottom-right-radius: 95rpx;
		// background-color: red;
		}
	.fixed-box {
		pointer-events: none; 
		width: 100vw;
		height: 100vh;
		position: fixed;
		left: 2px;
		bottom: 0;
		z-index: 100000;
	}
	.fixed-button {
		pointer-events: auto;
		width: 110upx;
		height: 360upx;
		right: 0;
		left: auto;
		top: 60vh;
	} 
	.mainMenu{
		width: 90upx;
		height: 90upx;
		border-radius: 50%;
		background: #fff;
		position: absolute;
		left: 0;
		bottom: 0rpx; 
	 }
	 /* .posi{
		 width: 90upx;
		 height:347rpx!important;
		 position: absolute;
		 left: 10upx;
		 bottom: -270rpx;
		 z-index:-1;
		 display: flex;
		 align-items: center;
		 flex-direction: column;
		 border-top-left-radius: 50rpx;
		 border-top-right-radius: 50rpx;
		 border-bottom-left-radius: 50rpx;
		 border-bottom-right-radius: 50rpx;
	 }
	 .posi>image{
		 width: 50upx;
		 height: 50upx;
		 margin-top: 30rpx;
	 } */
	 
	/* 适配iphonex 有底部横条的 */
	@supports (bottom: constant(safe-area-inset-bottom)) or (bottom: env(safe-area-inset-bottom)) {
		.fixed-box {
			bottom: constant(safe-area-inset-bottom);
			bottom: env(safe-area-inset-bottom);
		}
	}

</style>
