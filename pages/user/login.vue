<template>
	<view class="login">
		<image src="/static/login/01221393ecb8162be07136d0bc8234d6@2x.png" mode="widthFix" class="top-background"></image>
		<image src="/static/login/LOGO@2x.png" mode="widthFix" class="logo"></image>
		<view class="input-area">
			<view class="input-group">
				<form>
					<view class="form-group">
						<input type="text" value="" placeholder="用户名/账号/手机号" class="username" />
						<i class="username-icon"></i>
					</view>
					<view class="view form-group">
						<input type="password" value="" placeholder="请输入您的密码" class="password" />
						<i class="password-icon"></i>
					</view>
					<button type="default">登录</button>
				</form>
			</view>
			<view class="auth-area">
				<view class="pass">
					<navigator url="../index/index">注册账号</navigator>
					<navigator url="../index/index">忘记密码</navigator>
				</view>
				<view class="slug">
					<image src="../../static/login/line.png" mode="widthFix"></image>
					<text>第三方账号登录</text>
					<image src="../../static/login/line.png" mode="widthFix"></image>
				</view>
				<view class="sass">
					<image src="../../static/login/weibo.png" mode="widthFix"></image>
					<image src="../../static/login/qq.png" mode="widthFix"></image>
					<image src="../../static/login/wexin.png" mode="widthFix"></image>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss" scoped>
	.login{
		.top-background{
			width: 750rpx;
			height: 650rpx;
			border-bottom-left-radius: 30%;
			border-bottom-right-radius: 30%;
		}
		.logo{
			width: 253rpx;
			position: absolute;
			top: 155rpx;
			left: 253rpx;
		}
		.input-area{
			width: 639rpx;
			height: 800rpx;
			background: #FFFFFF;
			box-shadow: 0rpx 10rpx 40rpx 0rpx rgba(223, 223, 223, 0.91);
			border-radius: 28rpx;
			position: absolute;
			top: 394rpx;
			left: 57rpx;
			.input-group{
				padding: 85rpx 39rpx;
				input{
					width: 457rpx;
					height: 88rpx;
					background: #F8F8F8;
					border-radius: 14rpx;
					padding-left: 104rpx;
					margin-bottom: 29rpx;
					font-size: 28rpx;
				}
				button{
					width: 561rpx;
					height: 88rpx;
					background: linear-gradient(90deg, #6688EB, #A947F4);
					border-radius: 44rpx;
					font-size: 33rpx;
					font-family: NotoSansHans;
					font-weight: 400;
					color: #FFFFFF;
					margin-top: 30rpx;
				}
				.form-group{
					position: relative;
					i{
						position: absolute;
						width: 28rpx;
						height: 36rpx;
						background-repeat: no-repeat;
						background-position: 0rpx 0rpx;
						top: 0rpx;
						background-size: 28rpx 36rpx;
						top: 25rpx;
						left: 40rpx;
					}
					.username-icon{
						background-image: url(../../static/login/username.png);
					}
					.password-icon{
						background-image: url(../../static/login/password.png);
					}
				}
			}
			.auth-area{
				padding: 0 53rpx;
				.pass{
					display: flex;
					flex-direction: row;
					justify-content: space-around;
					navigator{
						width: 100rpx;
						height: 24rpx;
						font-size: 24rpx;
						font-family: NotoSansHans;
						font-weight: 400;
						color: #666666;
					}
				}
				.slug{
					display: flex;
					flex-direction: row;
					color: #B3B8D3;
					font-size: 22rpx;
					justify-content: space-around;
					align-items: center;
					margin-top: 82rpx;
					image{
						width: 146rpx;
					}
				}
				.sass{
					display: flex;
					flex-direction: row;
					justify-content: space-around;
					align-items: center;
					margin-top: 53rpx;
					image{
						width: 87rpx;
					}
				}
			}
		}
	}
</style>
