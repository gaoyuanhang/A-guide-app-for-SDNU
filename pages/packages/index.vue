<template>
	<view class="content">
		<view class="uni-list">
			<view class="uni-list-cell" hover-class="uni-list-cell-hover" v-for="(item,index) in numbers" :key="index" @tap="openinfo" :data-newsid="item.post_id">
				<view class="uni-media-list">
					<image class="uni-media-list-logo" :src="item.author_avatar"></image>
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
					{id: "1", title: '山师新闻学子荣获中国新闻奖最高荣誉',author_avatar:'http://xiaoqing.sdnu.edu.cn/__local/E/85/E0/FAC727B5E83CB81B81A88CC3E3A_D41C5C9C_2DE3A.jpg',created_at:'2020-11-09',post_id:'001'}, 
					{id: "2", title: '刘庆慧：“教书先生”始于1978年的西藏故事',author_avatar:'http://xiaoqing.sdnu.edu.cn/__local/4/1D/1B/441FB1FC1CAE7A00EB80D9672C3_C184147B_3944E.jpg',created_at:'2020-10-17',post_id:'002'}, 
					{id: "3", title: '幸遇良师',author_avatar:'http://xiaoqing.sdnu.edu.cn/__local/D/B9/89/143200CA4A670AAB7148BCB8190_EE7D8436_41C6A.jpg',created_at:'2020-10-13',post_id:'003'},
					{id: "4", title: '“王老师信箱”的1164封“家书”',author_avatar:'http://xiaoqing.sdnu.edu.cn/__local/9/60/3E/81FB9327F4DA64687C20C8EA3D8_34F1E297_2DBC3.jpg',created_at:'2020-09-11',post_id:'004'},
					{id: "5", title: '最好的时光',author_avatar:'http://xiaoqing.sdnu.edu.cn/__local/5/5A/D3/AD5B4BA1300D8A2B2629556057C_CD32760F_56AFE.jpg',created_at:'2020-09-04',post_id:'005'},
					{id: "6", title: '小草对母校的呢喃',author_avatar:'http://xiaoqing.sdnu.edu.cn/__local/D/98/3C/5B342D95AD2BE326CE87DD5A6B5_6E70AE4E_2F788.jpg',created_at:'2020-09-01',post_id:'006'},
					{id: "7", title: '我们家与山师的60年',author_avatar:'http://xiaoqing.sdnu.edu.cn/__local/1/5B/F1/B6555DAEA0BB88233E955858F76_17CA1BB0_8E588.png',created_at:'2020-08-31',post_id:'007'},
					{id: "8", title: '四年，一辈子——写在母校70周年校庆之际',author_avatar:'http://xiaoqing.sdnu.edu.cn/__local/3/79/BA/52AB480E1235972AC05B76A4802_B3C31C8D_49C6.jpg',created_at:'2020-08-26',post_id:'008'},
					{id: "9", title: '畅想十月',author_avatar:'http://xiaoqing.sdnu.edu.cn/__local/F/52/F6/5C71EE7A43C56A2522B43F88812_D02F2F65_7197.jpg',created_at:' 2020-08-25',post_id:'009'},
					{id: "10", title: '天下桃李 感恩母校',author_avatar:'http://xiaoqing.sdnu.edu.cn/__local/B/76/47/8E0A5A2E70FB0B6E0E6BCE88722_CFE75985_18C3D.jpg',created_at:' 2020-08-18',post_id:'010'},
					{id: "11", title: '那些仍带着温度的记忆',author_avatar:'http://xiaoqing.sdnu.edu.cn/__local/2/D7/9A/E8A65B7F2ED460EE496879D3B30_25137B11_8E2C4.png',created_at:' 2020-08-14',post_id:'011'},
					{id: "12", title: '奠基础 谋发展 求提高——看母校数学学科发展历程',author_avatar:'http://xiaoqing.sdnu.edu.cn/__local/D/43/20/BB1C4E68BD6B054DF314B39A981_A91A6784_7CA0.jpg',created_at:'2020-08-14',post_id:'012'},
					{id: "13", title: '明月寄相思 万里忆校园——写在母校70年校庆之际',author_avatar:'http://xiaoqing.sdnu.edu.cn/__local/F/C0/46/A495B94180EC230FF45C33074EC_EEFC183C_69DC5.jpg',created_at:' 2020-08-13',post_id:'013'},
				
				],
			};
		},
		
		methods:{
			openinfo(e) {
				console.log(e);
				var newsid = e.currentTarget.dataset.newsid;
				switch(newsid){
					case '001':{
						uni.navigateTo({url: '../info/info?newsid='+newsid});
						break;
					}
					case '002':{
						uni.navigateTo({url: '../info/info2?newsid='+newsid});
						break;
					}
					case '003':{
						uni.navigateTo({url: '../info/info3?newsid='+newsid});
						break;
					}
					case '004':{
						uni.navigateTo({url: '../info/info4?newsid='+newsid});
						break;
					}
					case '005':{
						uni.navigateTo({url: '../info/info5?newsid='+newsid});
						break;
					}
					case '006':{
						uni.navigateTo({url: '../info/info6?newsid='+newsid});
						break;
					}
					case '007':{
						uni.navigateTo({url: '../info/info7?newsid='+newsid});
						break;
					}
					case '008':{
						uni.navigateTo({url: '../info/info8?newsid='+newsid});
						break;
					}
					case '009':{
						uni.navigateTo({url: '../info/info9?newsid='+newsid});
						break;
					}
					case '010':{
						uni.navigateTo({url: '../info/info10?newsid='+newsid});
						break;
					}
					case '011':{
						uni.navigateTo({url: '../info/info11?newsid='+newsid});
						break;
					}
					case '012':{
						uni.navigateTo({url: '../info/info12?newsid='+newsid});
						break;
					}
					case '013':{
						uni.navigateTo({url: '../info/info13?newsid='+newsid});
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
