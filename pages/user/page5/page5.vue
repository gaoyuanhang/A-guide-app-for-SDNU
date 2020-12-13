<template>
	<view>
		<view>
			<view class="icon">
				<image src="/static/山师图片.jpg"></image>
			</view>
		</view>
		
		<view class="name">
		<view class="hh">山东师范大学</view>
		</view>
		
		<view class="m1">软件制作人：</view>
		<view class="name1">
		<view class="m">高** </view>
		<view class="m">高**</view>
		<view class="m">刘**</view>
		<view class="m">姜**</view>
		<view class="m">徐**</view>
		<view class="m">王**</view>
		<view class="m">(排名不分先后)</view>
		</view>
		<view class="banquan">
			<text class="num">Copytight  2020-2021\n</text>
			<text class="num">山东师范大学 版权所有</text>
		</view>
</view>

</template>

<script>
	// export default {
	// 	computed: mapState(['forcedLogin', 'hasLogin', 'userName']),
	// 	onLoad() {
	// 		const loginType = uni.getStorageSync('login_type')
	// 		if (loginType === 'local') {
	// 			this.login(uni.getStorageSync('username'))
	// 			return
	// 		}
	// 		let uniIdToken = uni.getStorageSync('uniIdToken')
	// 		if (uniIdToken) {
	// 			this.login(uni.getStorageSync('username'))
	// 			uniCloud.callFunction({
	// 				name: 'user-center',
	// 				data: {
	// 					action: 'checkToken',
	// 				},
	// 				success: (e) => {
	
	// 					console.log('checkToken success', e);
	
	// 					if (e.result.code > 0) {
	// 						//token过期或token不合法，重新登录
	// 						if (this.forcedLogin) {
	// 							uni.reLaunch({
	// 								url: '../login/login'
	// 							});
	// 						} else {
	// 							uni.navigateTo({
	// 								url: '../login/login'
	// 							});
	// 						}
	// 					}
	// 				},
	// 				fail(e) {
	// 					uni.showModal({
	// 						content: JSON.stringify(e),
	// 						showCancel: false
	// 					})
	// 				}
	// 			})
	// 		} else {
	// 			this.guideToLogin()
	// 		}
	// 	}
	// 	}
</script>

<style lang="scss">
	// @import url("../../../components/watch-login/css/icon.css");
	// @import url("./css/main.css");
// .header {
// 	width:161rpx;
// 	height:161rpx;
// 	box-shadow:0rpx 0rpx 60rpx 0rpx rgba(0,0,0,0.1);
// 	border-radius:50%;
// 	background-color: #000000; 
// 	// margin-top: 50rpx;
// 	// margin-bottom: 72rpx;
// 	// margin-left: auto;
// 	// margin-right: auto;
// }
.icon image{
	width:161rpx;
	height:161rpx;
	border-radius:50%;
	margin-left: 40%;
	margin-top: 30%;
	
}
.icon{
	width: 750rpx;
	height:161rpx;
	display: flex;
	align-items: center;
}
// .header{
// 	width:161rpx;
// 	height:161rpx;
// }
.name{
	margin-top: 20%;
}
.name1{
	margin-left: 35%;
	margin-top: -8%;
}
.hh{
	font-size: 18px;
	font-family: "隶书";
	margin-top: 25px;
	text-align: center;
}
.m1{
	font-size: 18px;
	font-family: "隶书";
	margin-left: 15rpx;
	margin-top: 100rpx;
}
.m{
	font-size: 14px;
	font-family: "隶书";
	margin-left: 20rpx;
	margin-top: 25rpx;
	// margin:0 auto;
	letter-spacing:15rpx;
}
.banquan{
	margin-top: 30%;
	text-align: center;
}
.num{
	font-size: 14px;
	font-family: "隶书";
}
</style>
