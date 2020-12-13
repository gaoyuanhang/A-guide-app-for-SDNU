<template>
	<view class="article">
		<swiper class="swiper":indicator-dots="true":autoplay="true":interval="4000":duration="2000">
			<swiper-item>
				<view class="swiper-item uni-bg-red">
				<view class="picture">
					<!-- 文章开头，缩略图 -->
					<image class="banner-img" src="/static/library.jpg" mode="widthFix"></image>
					<!-- 文章摘要 -->
					<!--<view class="picture-title">
						<text class="uni-ellipsis">...</text>
					</view>-->
				</view>
				</view>
			</swiper-item>
		</swiper>
		<!--<view class="title">山东师范大学图书馆</view>-->
		<view>
			<view class="intro">内容简介</view>
		</view>
		<!-- 新闻详情：使用 uParse 解析富文本-->
		<view class="article-content">
			<text>
      山东师范大学图书馆始建于1950年，前身是山东师范学院图书馆。现有工作人员95人，设有办公室、资源建设部、系统部、读者服务一部、读者服务二部、参考咨询与学科服务部、特藏研究部、情报研究服务部、技术服务中心、宣传推广中心。另设有学术委员会、青年工作委员会、学生工作委员会暨志愿者工作指导委员会等组织。

图书馆功能定位为学校信息资源中心、读者学习中心和学术与文化交流中心；服务宗旨为“读者至上，服务第一”。

      长清湖校区图书馆建筑面积50934.67平方米，是按照图书馆功能定位要求建设的现代化新馆，2015年6月开始运行。主体建筑呈“八本书”造型，为学校标志性景观，被誉为“天地书声”。可容纳纸质藏书200万册，设置阅览座位4600余个，设有读者学习、学术研修、综合服务、特藏阅览、信息共享与创客、展览交流、齐鲁文化展示、中外文化交流等八大空间和特藏、齐鲁文化、师大文库、外文、样本、基藏等六大书库，还建有咖啡厅、书吧等服务设施。

      图书馆收藏书刊共计407.5万余册。其中，中外文图书374.5万余册，中、外文期刊9600余种，33万余册。购置电子图书287万余册，中、外文数据库193个。馆藏线装古籍20万册（善本古籍1120种，15688册）。有36和462种古籍分别入选国家和山东省珍贵古籍名录，是全国和山东省古籍重点保护单位。

      图书馆重视信息技术应用和数字化图书馆建设。馆内系统采用较为先进的虚拟存储系统，构建了数字图书馆门户系统，建设了较为完善的馆藏书目数据库，引进了汇文自动化管理系统和中外文资源发现系统、移动图书馆、馆际互借与原文传递系统、随书光盘系统、远程访问系统等。拥有智能化管理平台、自助借还、门禁管理、楼宇智能管理等先进系统及设备，其中智能管理平台将3D导航、信息发布、研修间预约、座位管理、读者互动、检索等六个系统集成，为读者提供快捷高效服务。
          </text>
	 <view class="time">
	 <image class="banner-img" src="/static/library_time.jpg" mode="widthFix"></image>
	 </view>
		 <text>注：1）图书馆开馆时间随学校作息时间而变动，请随时注意图书馆通知。

2）馆藏分布如有变动，以图书馆通知为准；</text>
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
