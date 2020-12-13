<template>
	<view class="article">
		<swiper class="swiper":indicator-dots="true":autoplay="true":interval="4000":duration="2000":circular="true">
			<swiper-item>
				<view class="swiper-item uni-bg-red">
				<view class="picture">
					<image class="banner-img" src="/static/canteen2_face.jpg" mode="widthFix"></image>
					<!--<view class="picture-title">
						<text class="uni-ellipsis">...</text>
					</view>-->
				</view>
				</view>
			</swiper-item>
			<swiper-item>
			<view class="picture">
				<!-- 文章开头，缩略图 -->
				<image class="banner-img" src="/static/canteen2_behind.jpg" mode="widthFix"></image>
				<!-- 文章摘要 -->
				<!--<view class="picture-title">
					<text class="uni-ellipsis">...</text>
				</view>-->
			</view>
			</swiper-item>
		</swiper>
		<!--<view class="title">第二餐厅</view>-->
		<view>
			<view class="intro">内容简介</view>
		</view>
		<!-- 新闻详情：使用 uParse 解析富文本-->
			<view class="article-content">
						<text>
							美食商家群英荟萃，碰撞出美味的另一种新可能。
							
							一楼的小店分布可谓密密麻麻，二楼则提供了大量的餐位。建筑的后门提供了可供聚餐的一方小天地。
						</text>
						<text>
							麻雀虽小，五脏俱全，用这句话来形容这些小店再适合不过了。
							
							走进二餐，方知人间至味是鲜美 。鲜美滑爽的螺蛳粉，酸、辣、鲜、爽、烫；香酥可口的大煎饼，自带山东的味道；皮薄馅多的水饺，感受家的味道；大朋友小朋友都爱喝的奶茶，在寒冷的冬天带来些许，温暖；
							掉渣饼，热干面，麻辣香锅，麻辣烫，布袋馍，炸串，老母鸡汤，来自全国各地的特色小吃，每一个都会给你带来不一样的味道！
			       </text>
			<view class="picture">
			<image class="banner-img" src="/static/lsf.jpg" mode="widthFix"></image>
			<view class="picture-title">
				<text class="uni-ellipsis">螺蛳粉</text>
			</view>
			</view>
			<view class="picture">
			<image class="banner-img" src="/static/sjb.jpg" mode="widthFix"></image>
			<view class="picture-title">
				<text class="uni-ellipsis">一楼生煎包</text>
			</view>
			</view>
			<view class="picture">
			<image class="banner-img" src="/static/ppj.jpg" mode="widthFix"></image>
			<view class="picture-title">
				<text class="uni-ellipsis">二楼泡泡鸡</text>
			</view>
			</view>
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










