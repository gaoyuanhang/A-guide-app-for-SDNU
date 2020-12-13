<template>
	<view class="article">
		<swiper class="swiper":indicator-dots="true":autoplay="true":interval="4000":duration="2000">
			<swiper-item>
				<view class="swiper-item uni-bg-red">
				<view class="picture">
					<image class="banner-img" src="/static/gymnasium3.jpg" mode="widthFix"></image>
					<!--<view class="picture-title">
						<text class="uni-ellipsis">...</text>
					</view>-->
				</view>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="picture">
					<image class="banner-img" src="/static/gymnasium1.jpg" mode="widthFix"></image>
					<!--<view class="picture-title">
						<text class="uni-ellipsis">...</text>
					</view>-->
				</view>
			</swiper-item>
		</swiper>
		<!--<view class="title">体育馆</view>-->
		<view>
			<view class="intro">内容简介</view>
		</view>
		<!-- 新闻详情：使用 uParse 解析富文本-->
		<view class="article-content">
			<text>
                体育馆共有两层。
				一楼主要是供体育训练和体育课的场所。
				二楼有篮球场、羽毛球场。
			</text>
	    </view>
	</view>
</template>

<script>
	
</script>

<style>

	/* 标题 */
	.title {
			margin-left: 20px;
			font-size: 15px;
			font-family: "微软雅黑";
			color: #F55C23;
	}
	
	.intro {
			//position: absolute;
			width: 110px;
			height: 35px;
			//margin-top: 10px;
			//left: 100px;
			margin:10px auto;
			background-color: #66AAFF;
			font-size: 14px;
			font-weight: bold;
			font-family: "黑体";
			color: white;
			text-align: center;
			padding:5px 20px;
			border: white;
			border-radius: 25px;
			border-width: 5px;
			border-style: double;
	}
	
	.swiper{
	height: 180px;
	}

	.picture {
		position: relative;
		//margin: 0 15px;
		height: 180px;
		overflow: hidden;
	}
	
	.time {
		position: relative;
		height: 300px;
		overflow: hidden;
	}

	.banner-img {
		position: absolute;
		width: 100%;
	}

	.picture-title {
		display: flex;
		align-items: center;
		position: absolute;
		padding: 0 15px;
		width: 100%;
		bottom: 0;
		height: 30px;
		font-size: 14px;
		color: #fff;
		background: rgba(0, 0, 0, 0.4);
		overflow: hidden;
		box-sizing: border-box;
	}

	.uni-ellipsis {
		overflow: hidden;
		white-space: nowrap;
		text-overflow: ellipsis;
	}

	.article-content {
		//margin-top: 70px;
		padding:0 15px;
		font-size: 15px;
		overflow: hidden;
		font-family: "华文中宋";
	}
</style>