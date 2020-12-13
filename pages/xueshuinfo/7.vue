<template>
	<view class="container">
		
		<image src="http://acad.cnki.net/fengmian/CJFD/big/sdzk.jpg"mode="widthFix"></image>
		
		<view>
			COMPACT DIFFERENCE SCHEME FOR ONE-DIMENSIONAL FRACTIONAL CATTANEO EQUATION
			王小菡;姜子文;
			Wang Xiaohan;Jiang Ziwen;School of Mathematics and Statistics,Shandong Normal University;
			1:山东师范大学数学与统计学院
			摘要(Abstract)：
			
			传统的Fick定律是描述扩散(热传导)现象的基本定律.由于此定律不涉及时间项,因而就隐含了传播速度无限大的不合理假设.有许多研究成果试图修正传统的Fick定律,其中最著名的是Cattneo模型.从CTRW理论、非局部传输理论和延迟通量力的关系三种不同的角度,Compte和Metzler将Cattneo模型推广到了时间分数阶Cattneo模型.本文针对一维推广的分数阶Cattaneo方程提出了一种紧致有限差分格式,该格式对时间分数阶导数采用L1逼近,对空间整数阶导数采用四阶紧差分算子逼近.数值算例验证了该格式的收敛阶为o(τ~(2-α)+h~4).
			The Fick law is adopted as basic model for the description of heat and mass transfer. But the validity of using this law has been questioned extensively. The main reason is that this law implies an infinite velocity of propagation. In order to consider the finite velocity of propagation, several new constitutive models have been introduced, for example, the widely used Cattaneo model. Recently, Compte and Metzler generalized the Cattaneo model to the time fractional models, which was supported by three different scheme: continuous time random walks, non-local transport theory, and delayed flux-force relation. In this paper, a compact finite difference method is proposed for the one-dimensional generalized fractional Cattaneo equation, which adopts L1 approximation for the time fractional derivative and compact approximation for the space integer derivative. A numerical example shows that the convergence order of the scheme is o(τ~(2-α)+h~4).
			
			关键词(KeyWords)： 分数阶Cattaneo方程;L1逼近;紧致差分格式
			fractional Cattaneo equation;L1 approximation;compact difference scheme
			
			基金项目(Foundation): 国家自然科学基金资助项目(11171193);; 山东省自然科学基金资助项目(ZR2017MA020)
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
