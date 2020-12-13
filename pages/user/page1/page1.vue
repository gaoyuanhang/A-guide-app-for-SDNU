<template>
  <view>
    <cmd-nav-bar back title="信息设置"></cmd-nav-bar>
    <cmd-page-body type="top">
      <cmd-transition name="fade-up">
        <view>
          <cmd-cel-item title="头像" slot-right arrow>
            
			<!-- #ifdef MP-WEIXIN -->
			<cmd-avatar :src="avatarUrl"></cmd-avatar>
			<!-- #endif -->
			<!-- #ifdef APP-PLUS -->
			<cmd-avatar src="../../../static/img/logo.png"></cmd-avatar>
			<!-- #endif -->
			<!-- #ifdef H5 -->
			<cmd-avatar src="../../../static/img/logo.png"></cmd-avatar>
			<!-- #endif -->
			
          </cmd-cel-item>
          <!-- <cmd-cel-item title="积分" addon="566" arrow></cmd-cel-item> -->
          <cmd-cel-item title="昵称" :addon="userName" arrow></cmd-cel-item>
          <!-- <cmd-cel-item title="姓名" addon="Lich" arrow></cmd-cel-item> -->
          <!-- <cmd-cel-item title="联系方式" addon="15676109501" arrow></cmd-cel-item> -->
          <!-- <cmd-cel-item title="证件号码" addon="450112xxxxxxxx2017" arrow></cmd-cel-item> -->
          <cmd-cel-item title="我的地址" addon="山东师范大学长清湖校区" arrow></cmd-cel-item>
          <!-- <cmd-cel-item title="修改密码" @click="fnClick('modify')" arrow></cmd-cel-item> -->
          <!-- <button class="btn-logout">退出登录</button> -->
		  
		  <view class="btn-row">
		  	<button v-if="hasLogin" class="primary" type="primary" @tap="bindLogout">退出登录</button>
		  </view>
        </view>
      </cmd-transition>
    </cmd-page-body>
  </view>
</template>

<script>
  import cmdNavBar from "@/components/cmd-nav-bar/cmd-nav-bar.vue"
  import cmdPageBody from "@/components/cmd-page-body/cmd-page-body.vue"
  import cmdTransition from "@/components/cmd-transition/cmd-transition.vue"
  import cmdCelItem from "@/components/cmd-cell-item/cmd-cell-item.vue"
  import cmdAvatar from "@/components/cmd-avatar/cmd-avatar.vue"
import {
		mapState,
		mapMutations
	} from 'vuex'
  export default {
	  computed: mapState(['forcedLogin', 'hasLogin', 'userName']),
	  		onLoad() {
	  			const loginType = uni.getStorageSync('login_type')
	  			if (loginType === 'local') {
	  				this.login(uni.getStorageSync('username'))
	  				return
	  			}
	  			let uniIdToken = uni.getStorageSync('uniIdToken')
	  			if (uniIdToken) {
	  				this.login(uni.getStorageSync('username'))
	  				uniCloud.callFunction({
	  					name: 'user-center',
	  					data: {
	  						action: 'checkToken',
	  					},
	  					success: (e) => {
	  
	  						console.log('checkToken success', e);
	  
	  						if (e.result.code > 0) {
	  							//token过期或token不合法，重新登录
	  							if (this.forcedLogin) {
	  								uni.reLaunch({
	  									url: '../login/login'
	  								});
	  							} else {
	  								uni.navigateTo({
	  									url: '../login/login'
	  								});
	  							}
	  						}
	  					},
	  					fail(e) {
	  						uni.showModal({
	  							content: JSON.stringify(e),
	  							showCancel: false
	  						})
	  					}
	  				})
	  			} else {
	  				this.guideToLogin()
	  			}
	  		},
	  
	  
    components: {
      cmdNavBar,
      cmdPageBody,
      cmdTransition,
      cmdCelItem,
      cmdAvatar
    },

    data() {
      return {
		  avatarUrl: "../../static/img/logo.png",
		  inviteUrl: ''
	  };
    },

    mounted() {},
    
    methods:{
		...mapMutations(['logout']),
		...mapMutations(['login']),
					guideToLogin() {
						uni.showModal({
							title: '未登录',
							content: '您未登录，需要登录后才能继续',
							/**
							 * 如果需要强制登录，不显示取消按钮
							 */
							showCancel: !this.forcedLogin,
							success: (res) => {
								if (res.confirm) {
									/**
									 * 如果需要强制登录，使用reLaunch方式
									 */
									if (this.forcedLogin) {
										uni.reLaunch({
											url: '../login/login'
										});
									} else {
										uni.navigateTo({
											url: '../login/login'
										});
									}
								}
							}
						});
					},
					bindLogout() {
						const loginType = uni.getStorageSync('login_type')
						if (loginType === 'local') {
							this.logout();
							if (this.forcedLogin) {
								uni.reLaunch({
									url: '../login/login',
								});
							}
							return
						}
					uniCloud.callFunction({
							name: 'user-center',
							data: {
								action: 'logout'
							},
							success: (e) => {
					
								console.log('logout success', e);
					
								if (e.result.code == 0) {
									this.logout();
									uni.removeStorageSync('uniIdToken')
									uni.removeStorageSync('username')
									/**
									 * 如果需要强制登录跳转回登录页面
									 */
									this.inviteUrl = ''
									if (this.forcedLogin) {
										uni.reLaunch({
											url: '../login/login',
										});
									}
								} else {
									uni.showModal({
										content: e.result.msg,
										showCancel: false
									})
									console.log('登出失败', e);
								}
					
							},
							fail(e) {
								uni.showModal({
									content: JSON.stringify(e),
									showCancel: false
								})
							}
						})
					},
		
      /**
       * 点击触发
       * @param {Object} type 跳转页面名或者类型方式
       */
      fnClick(type){
        if(type == 'modify'){
          uni.navigateTo({
            url:'/pages/user/page5/page5'
          })
        }
      }
    }
  }
</script>

<style>
  .btn-logout {
    margin-top: 100upx;
    width: 80%;
    border-radius: 50upx;
    font-size: 16px;
    color: #fff;
    background: linear-gradient(to right, #365fff, #36bbff);
  }

  .btn-logout-hover {
    background: linear-gradient(to right, #365fdd, #36bbfa);
  }
</style>
