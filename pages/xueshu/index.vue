<template>
	<view class="content">
		<view class="uni-list">
			<view class="uni-list-cell" hover-class="uni-list-cell-hover" v-for="(item,index) in numbers" :key="index" @tap="openinfo" :data-newsid="item.post_id">
				<view class="uni-media-list">
					<image class="uni-media-list-logo" :src="item.cover"></image>
					<view class="uni-media-list-body">
						<view class="uni-media-list-text-top">{{item.title}}</view>
						<view class="uni-media-list-text-bottom uni-ellipsis">{{item.created_at}}</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				numbers:[
					
					{id: "1",title:"张文新教授3篇学术论文被国际发展心理学权威教科书《青少年期》",cover: "http://www.skc.sdnu.edu.cn/__local/2/E8/2A/8A0035C89A15B5E393F700F5DF9_419B7703_163CA.jpg",created_at: "2020-04-11 17:11:09",post_id:'11',},
					{id: "2",title: "学校召开国家级社科重大项目培育研讨会",cover: "http://www.skc.sdnu.edu.cn/__local/C/6C/0E/A8C2D82259092E355524B8FCC12_8B294B50_14FF2.jpg",created_at: "2020-12-06 17:11:09",post_id:'12',},
				    {id: "3",title: "重磅！山东师范大学喜获国家自然科学奖二等奖",cover: "http://www.kjc.sdnu.edu.cn/__local/B/B6/A8/EC57A9871A42CCB27A514784505_88DD99FF_299F7.jpg",created_at: "2020-04-11 17:11:09",post_id:'13',},
					{id: "4",title: "学校召开科技成果转移转化工作领导小组会议",cover: "http://www.kjc.sdnu.edu.cn/__local/8/BF/34/7AE56E99DC943CFC9E51B560BA7_28DBCD7F_9503.jpg",created_at: "2020-04-11 17:11:09",post_id:'14',},
					{id: "5",title: "国家自然科学基金委员会交叉科学高端学术论坛在京召开",cover: "http://www.nsfc.gov.cn/Portals/0/images/news_images/tpxw2020-11-29-04.jpg",created_at: "2020-04-11 17:11:09",post_id:'15',},
					{id: "6",title: "我校承办第五届数学、系统与控制交叉研究青年论坛暨《中国科学：信息科学》座谈会",cover: "http://www.kjc.sdnu.edu.cn/__local/F/50/66/9C69BDCBDE901B9D87AB390B298_14CF8419_1F0BD.png",created_at: "2020-04-11 17:11:09",post_id:'16',},
					{id: "7",title: "山东师范大学学报(自然科学版)",cover: "http://acad.cnki.net/fengmian/CJFD/big/sdzk.jpg",created_at: "2020-04-11 17:11:09",post_id:'17',},
					{id: "8",title: "关于组织开展2020年度山东省农业良种工程项目申报的通知",cover: "http://www.skc.sdnu.edu.cn/images/syban_01.jpg",created_at: "2020-04-11 17:11:09",post_id:'18',},
					{id: "9",title: "关于做好研究阐释党的十九届五中全会精神国家社科基金重大项目招标工作的通知",cover: "http://www.qlshx.sdnu.edu.cn/__local/F/BE/E3/5BC99FDAAF0A60D2E12F4291CED_9CAE6A2E_16FEB.jpg",created_at: "2020-04-11 17:11:09",post_id:'19',},
					{id: "10",title: "‍‍关于做好2021年度国家社科基金艺术学重大项目招标选题征集工作的通知",cover: "http://www.qlshx.sdnu.edu.cn/__local/9/4A/F6/221F2BA516B52FA6C2B0A01F9B1_92155A40_390BF.png",created_at: "2020-04-11 17:11:09",post_id:'20',},
													
					
						

				],
			};
		},
		
		methods:{
			openinfo(e) {
				console.log(e);
				var newsid = e.currentTarget.dataset.newsid;
				switch(newsid){
					case '11':{
						uni.navigateTo({url: '../xueshuinfo/1?newsid='+newsid});
						break;
					}
					case '12':{
						uni.navigateTo({url: '../xueshuinfo/2?newsid='+newsid});
						break;
					}
					case '13':{
						uni.navigateTo({url: '../xueshuinfo/3?newsid='+newsid});
						break;
					}
					case '14':{
						uni.navigateTo({url: '../xueshuinfo/4?newsid='+newsid});
						break;
					}case '15':{
						uni.navigateTo({url: '../xueshuinfo/5?newsid='+newsid});
						break;
					}case '16':{
						uni.navigateTo({url: '../xueshuinfo/6?newsid='+newsid});
						break;
					}case '17':{
						uni.navigateTo({url: '../xueshuinfo/7?newsid='+newsid});
						break;
					}case '18':{
						uni.navigateTo({url: '../xueshuinfo/8?newsid='+newsid});
						break;
					}case '19':{
						uni.navigateTo({url: '../xueshuinfo/9?newsid='+newsid});
						break;
					}case '20':{
						uni.navigateTo({url: '../xueshuinfo/10?newsid='+newsid});
						break;
					}
					
					default:break;
					}	
				}
				}
				}
</script>

<style>
	.uni-media-list-body{height:auto;}
	.uni-media-list-text-top{line-height: 1.6em;}
</style>
