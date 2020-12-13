<template>
	<view class="article">
		<swiper class="swiper":indicator-dots="true":autoplay="true":interval="4000":duration="2000">
			<swiper-item>
				<view class="swiper-item uni-bg-red">
				<view class="picture">
					<!-- 文章开头，缩略图 -->
					<image class="banner-img" src="/static/hospital.jpg" mode="widthFix"></image>
					<!-- 文章摘要 -->
					<!--<view class="picture-title">
						<text class="uni-ellipsis">...</text>
					</view>-->
				</view>
				</view>
			</swiper-item>
		</swiper>
		<!--<view class="title">山东师范大学校医院</view>-->
		<view>
			<view class="intro">内容简介</view>
		</view>
		<!-- 新闻详情：使用 uParse 解析富文本-->
		<view class="article-content">
			<text>
                校医院的前身是校卫生室，1952年建立，1978年改制成为保健科。
				
      	        山师大医院现设有综合门诊（学生、教工综合门诊）、中医、理疗、五官、心电图、检验、放射、B超室、注射室、观察室、供应室、换药室、预防保健、挂号收款室,设有院办公室、大学生医保、省直医保、计划生育办公室等管理科室。
				
                1995年，山师大医院被评审为"一级甲等医院"，1998年成立山东师范大学社区卫生服务站，先后为2000多户居民建立健康档案，并签订了家庭卫生保健协议，极大的方便了教职工就医，受到了患者和有关部门的好评。2003年在抗击"非典"的战斗中表现出色，受到国务院、省市区各级卫生行政部门的表彰。医院倡导临床医生一专多能，向全科医生的方向发展，努力探索社会主义市场经济条件下高校医院生存与发展的新路。
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

