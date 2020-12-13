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
					 
					{id: "01",title:'我校8门课程入选首批国家级一流本科课程',cover: "http://www.qlshx.sdnu.edu.cn/__local/2/01/78/A2B93391A94499D51C1799812AC_397B5BD7_60DA1.jpg",created_at: "2020-04-11 17:11:09",post_id:'11',address: "https://blog.csdn.net/JJ583500596/article/details/68944984"},
					{id: "02",title: "学校与中国农业银行山东省分行签订新一轮战略合作协议",cover: "http://www.qlshx.sdnu.edu.cn/__local/5/FC/F2/3BEB9AED1FEA37BAE3EC3095502_17ECB5F2_785DD.png",created_at: "2020-04-11 17:11:09",post_id:'12',address:"https://blog.csdn.net/JJ583500596/article/details/68944984",},
				    {id: "03",title: "学校举行2020年东岳学者聘任仪式",cover: "http://www.qlshx.sdnu.edu.cn/__local/1/8E/70/1F43AF31DDE87B4658BFCE870CF_5A5A62AC_10039.jpg",created_at: "2020-04-11 17:11:09",post_id:'13',address:"https://blog.csdn.net/JJ583500596/article/details/68944984",},
					{id: "04",title: "山东师大举行2020级新生开学典礼",cover: "http://www.qlshx.sdnu.edu.cn/__local/C/96/43/7D2E05B05C29D13047ED8C20EEF_948C8170_3A7B1.jpg",created_at: "2020-04-11 17:11:09",post_id:'14',address:"https://blog.csdn.net/JJ583500596/article/details/68944984",},
					{id: "05",title: "山东省副省长、中国工程院院士凌文到山师附小开展科普讲座",cover: "http://www.qlshx.sdnu.edu.cn/__local/D/16/21/169B20A21E6A32639FC9917E380_A9E4AEDE_44BF2.jpg",created_at: "2020-04-11 17:11:09",post_id:'15',address:"https://blog.csdn.net/JJ583500596/article/details/68944984",},
					{id: "06",title: "历史文化学院开展党员专题教育培训活动",cover: "http://www.qlshx.sdnu.edu.cn/__local/6/F2/FC/735C55E05D90ED966D9474E16BC_866A00B4_3BF43.jpg",created_at: "2020-04-11 17:11:09",post_id:'16',address:"https://blog.csdn.net/JJ583500596/article/details/68944984",},
					{id: "07",title: "地理与环境学院召开党员大会",cover: "http://www.qlshx.sdnu.edu.cn/__local/6/1C/AC/9ECDCB2942ECE52D749199D8FED_6840DDE1_2E450.jpg",created_at: "2020-04-11 17:11:09",post_id:'17',address:"https://blog.csdn.net/JJ583500596/article/details/68944984",},
					{id: "08",title: "中国劳动经济学学会会长扩大会议暨 “十四五”规划到2035年期间经济社会发展重大战略问题研讨会举办",cover: "http://www.qlshx.sdnu.edu.cn/__local/2/D1/56/1BABA83604FB1D3C3963C7BAEE5_18400C56_3DB93.jpg",created_at: "2020-04-11 17:11:09",post_id:'18',address:"https://blog.csdn.net/JJ583500596/article/details/68944984",},
					{id: "09",title: "中科院院士谭蔚泓一行来校交流访问",cover: "http://www.qlshx.sdnu.edu.cn/__local/F/BE/E3/5BC99FDAAF0A60D2E12F4291CED_9CAE6A2E_16FEB.jpg",created_at: "2020-04-11 17:11:09",post_id:'19',address:"https://blog.csdn.net/JJ583500596/article/details/68944984",},
					{id: "010",title: "学校举行儿童青少年发展暨第二届校园欺凌防治国际学术会议",cover: "http://www.qlshx.sdnu.edu.cn/__local/9/4A/F6/221F2BA516B52FA6C2B0A01F9B1_92155A40_390BF.png",created_at: "2020-04-11 17:11:09",post_id:'20',address:"https://blog.csdn.net/JJ583500596/article/details/68944984",},
					{id: "011",title: "我校承办2020泰山科技论坛暨山东省食品科学技术学会第八届年会",cover: "http://www.qlshx.sdnu.edu.cn/__local/1/83/96/9BAA9E6C89DB95C3AA25A4F6141_4D331B22_174DD.jpg",created_at: "2020-04-11 17:11:09",post_id:'21',address:"https://blog.csdn.net/JJ583500596/article/details/68944984",},
								 					
					
						

				],
			};
		},
		
		methods:{
			openinfo(e) {
				console.log(e);
				var newsid = e.currentTarget.dataset.newsid;
				switch(newsid){
					case '11':{
						uni.navigateTo({url: '../yaoweninfo/1?newsid='+newsid});
						break;
					}
					case '12':{
						uni.navigateTo({url: '../yaoweninfo/2?newsid='+newsid});
						break;
					}
					case '13':{
						uni.navigateTo({url: '../yaoweninfo/3?newsid='+newsid});
						break;
					}
					case '14':{
						uni.navigateTo({url: '../yaoweninfo/4?newsid='+newsid});
						break;
					}case '15':{
						uni.navigateTo({url: '../yaoweninfo/5?newsid='+newsid});
						break;
					}case '16':{
						uni.navigateTo({url: '../yaoweninfo/6?newsid='+newsid});
						break;
					}case '17':{
						uni.navigateTo({url: '../yaoweninfo/7?newsid='+newsid});
						break;
					}case '18':{
						uni.navigateTo({url: '../yaoweninfo/8?newsid='+newsid});
						break;
					}case '19':{
						uni.navigateTo({url: '../yaoweninfo/9?newsid='+newsid});
						break;
					}case '20':{
						uni.navigateTo({url: '../yaoweninfo/10?newsid='+newsid});
						break;
					}case '21':{
						uni.navigateTo({url: '../yaoweninfo/11?newsid='+newsid});
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
