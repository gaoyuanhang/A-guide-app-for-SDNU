<template>
	<view>
	<view class="content">
		<view class="flowPanel">
			<view class="leftPanel">
				<view class="itemContainer" v-for="(item,index) in flowList" :key="index" v-if="index%2==0">
					<img :src="item.image" mode="widthFix">
					<view class="title">{{item.title}}</view>
					<view class="info">
						<view class="left">
							<view class="date">{{item.date}}</view>
							<view class="commentNum">{{item.commentNum}}</view>
						</view>
						<view class="right">
							<view class="clickNum">{{item.clickNum}}</view>
						</view>
					</view>
				</view>
			</view>
			<view class="rightPanel">
				<view class="itemContainer" v-for="(item,index) in flowList" :key="index" v-if="index%2==1">
					<img :src="item.image" mode="widthFix">
					<view class="title">{{item.title}}</view>
					<view class="info">
						<view class="left">
							<view class="date">{{item.date}}</view>
							<view class="commentNum">{{item.commentNum}}</view>
						</view>
						<view class="right">
							<view class="clickNum">{{item.clickNum}}</view>
						</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</view>
</template>

<script>
	import dataJson from '../../viewData.js';
	export default {
		data() {
			return {
				flowList: [],
			}
		},
		async onLoad() {
			// load data
			this.flowList = dataJson.flowList;
		},
		methods: {
			
		},
		onPullDownRefresh() {
		        console.log('refresh');
		        setTimeout(function () {
		            uni.stopPullDownRefresh();
		        }, 1000);
		    }
	}
</script>

<style>
@charset "utf-8";
.flowPanel {
		flex-direction: row;
		justify-content: space-between;
		width: 100%;
		overflow: hidden;
	}
	
	.flowPanel .leftPanel {
		width: 48%;
		overflow: hidden;
	}
	
	.flowPanel .rightPanel {
		width: 48%;
		overflow: hidden;
	}
	
	.flowPanel .itemContainer {
		margin-top: 10px;
		position: relative;
		display:flex;
		flex-direction: column;
	}
	.flowPanel image {
		width: 100%;
	}
	
	.flowPanel .itemContainer .title {
		overflow: hidden;
		display: -webkit-box;
		-webkit-box-orient: vertical;
		-webkit-line-clamp: 2;
		word-wrap:break-word;
		word-break:break-all;
		color: #333;
		text-align: left;
		padding: 0.2em 0.5em;
	}
	
	.flowPanel .itemContainer .info {
		color: #8a8a8a;
		overflow: hidden;
		padding: 10px;
		border-top: 1px #e9e9e9 solid;
		flex-direction: row;
		justify-content: space-between;
	}
	.flowPanel .itemContainer .info .left {
		flex-direction: row;
	}
	.flowPanel .itemContainer .info .left .date {
		flex-direction: row;
		font-size: 11px;
		line-height: 11px;
	}
	.flowPanel .itemContainer .info .left .date:before {
		font-family: myfont;
		content: "\e63a"; 
		font-style: normal;
		-webkit-font-smoothing: antialiased;
		-webkit-text-stroke-width: .2px;
		padding-right: 2px;
	}
	.flowPanel .itemContainer .info .left .commentNum {
		padding-left: 5px;
		flex-direction: row;
		font-size: 11px;
		line-height: 11px;
	}
	.flowPanel .itemContainer .info .left .commentNum:before {
		font-family: myfont;
		content: "\e635";
		font-style: normal;
		-webkit-font-smoothing: antialiased;
		-webkit-text-stroke-width: .2px;
		padding-right: 2px;
	}
	.flowPanel .itemContainer .info .right {
		flex-direction: row;
	}
	.flowPanel .itemContainer .info .right .clickNum {
		flex-direction: row;
		font-size: 11px;
		line-height: 11px;
	}
	.flowPanel .itemContainer .info .right .clickNum:before {
		font-family: myfont;
		content: "\e633";
		font-style: normal;
		-webkit-font-smoothing: antialiased;
		-webkit-text-stroke-width: .2px;
		padding-right: 2px;
	}
	@font-face {
		font-family: "myfont";
		src: url("https://at.alicdn.com/t/font_1985981_791yzf7neql.ttf") format('truetype');
	}
	
	page{
		height: 100%; 
	}
	view{
		display:flex;
		flex-direction: column;
		box-sizing: border-box;
	}
	.content{
		width: 100%;
		background-color: #ffffff;
		padding: 0 15px;
	}
	
	
</style>