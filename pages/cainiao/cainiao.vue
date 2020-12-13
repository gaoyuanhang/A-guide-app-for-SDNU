<template>
	<view class="article">
		<swiper class="swiper":indicator-dots="true":autoplay="true":interval="4000":duration="2000">
			<swiper-item>
				<view class="swiper-item uni-bg-red">
				<view class="picture">
					<!-- 文章开头，缩略图 -->
					<image class="banner-img" src="/static/cainiao.jpg" mode="widthFix"></image>
					<!-- 文章摘要 -->
					<view class="picture-title">
						<text class="uni-ellipsis">菜鸟驿站门口</text>
					</view>
				</view>	
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item uni-bg-green">
					<view class="picture">
						<image class="banner-img" src="/static/cainiao_in.jpg" mode="widthFix"></image>
						<!-- 文章摘要 -->
						<view class="picture-title">
							<text class="uni-ellipsis">取件扫描处</text>
						</view>
					</view>
				</view>
			</swiper-item>
		</swiper>
		<!--<view class="title">菜鸟驿站</view>-->
		<view class="article-content">
			<text>
				开放时间：8:00--21:00
			</text>
		</view>
		<view>
			<view class="intro">内容简介</view>
		</view>	
		<!-- 新闻详情：使用 uParse 解析富文本-->
		<view class="article-content">
			<text>
			    菜鸟驿站位于二餐南侧的白色快递建筑群，规模庞大。另有京东快递。是学生寄取快递的热门场所。	
			</text>
	    </view>
	 </view>
</template>

<script>
	
</script>

<style>

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
	
	
	/* 标题 */
	.title {
			margin-left: 20px;
			font-size: 15px;
			font-family: "微软雅黑";
			color: #F55C23;
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
		//padding:0 15px;
		font-size: 15px;
		overflow: hidden;
		font-family: "华文中宋";
	}
	
</style>
