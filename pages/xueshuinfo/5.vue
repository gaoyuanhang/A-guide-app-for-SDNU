<template>
	<view class="container">
		
		<image src="	http://www.nsfc.gov.cn/Portals/0/images/news_images/tpxw2020-11-29-04.jpg" mode="widthFix"></image>
		
		<view>
			</view>
		
	</view>
</template>
//页面文件为.vue文件，遵循vue.js的单文档组件开发规范，一个页面（.ve）文件存在三个顶级语言模块template：模板层，用户看的见，官网组件自己学script:脚本层，vue.js自己学，接口自己学style：样式层，
<script>//data属性,对象的形式展示，键值对方式声明的，data必须声明为返回一个初始数据对象的函数，否则关闭页面时，数据不会自动销毁，再次打开页面会显示上次数据，
	export default {
	data() {
		return {
			
		}
	},
	}
</script>

<style>
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
	}
</style>
