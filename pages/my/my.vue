<template>
	<view>
		<view class="header">
			<view class="avatar">
				<image src="../../static/my/icon-11.png" mode="widthFix"></image>
				<text>小姐姐</text>
			</view>
			<view class="two-data">
				<view class="item">
					<text>我的收藏</text>
					<text>434</text>
				</view>
				<view class="item">
					<text>我的收藏</text>
					<text>23</text>
				</view>
			</view>
			<view class="one-data">
				<text>我的全部订单</text>
				<text>1356</text>
			</view>
		</view>
		<view class="platform">
			<image src="../../static/my/icon-1.png" mode="widthFix"></image>
			<view class="lines">
				<view class="one-line">
					<text>平台会员</text>
					<text>一年只要88</text>
				</view>
				<text>用大约40项会员特权</text>
			</view>
		</view>
		<view class="navs">
			<text class="title">我的订单</text>
			<view class="items">
				<navigator class="item" url="../order/order">
					<image src="../../static/my/icon-4.png" mode="widthFix"></image>
					<image src="../../static/my/icon-7.png" mode="widthFix"></image>
					<text>待付款</text>
				</navigator>
				<view class="item">
					<image src="../../static/my/icon-5.png" mode="widthFix"></image>
					<text>代发货</text>
				</view>
				<view class="item">
					<image src="../../static/my/icon-2.png" mode="widthFix"></image>
					<text>待收货</text>
				</view>
				<view class="item">
					<image src="../../static/my/icon-6.png" mode="widthFix"></image>
					<text>待评价</text>
				</view>
			</view>
		</view>
		<view class="menus">
			<view class="item">
				<view class="left">
					<image src="../../static/my/icon-8.png" mode="widthFix"></image>
					<text>我的钱包</text>
				</view>
				<i class="iconfont icon-right"></i>
			</view>
			<view class="item">
				<view class="left">
					<image src="../../static/my/icon-9.png" mode="widthFix"></image>
					<text>优惠券</text>
				</view>
				<i class="iconfont icon-right"></i>
			</view>
			<view class="item">
				<view class="left">
					<image src="../../static/my/icon-10.png" mode="widthFix"></image>
					<text>收藏夹</text>
				</view>
				<i class="iconfont icon-right"></i>
			</view>
			<navigator class="item" url="../user/login">
				<view class="left">
					<image src="../../static/my/icon-3.png" mode="widthFix"></image>
					<text>收获地址</text>
				</view>
				<i class="iconfont icon-right"></i>
			</navigator>
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
	.header{
		background-image: url(../../static/my/background.jpg);
		background-repeat: no-repeat;
		background-size: 100%;
		width: 750rpx;
		height: 500rpx;
		.avatar{
			display: flex;
			flex-direction: column;
			align-items: center;
			padding-top: 120rpx;
			image{
				width: 120rpx;
				border-radius: 50%;
			}
			text{
				margin-top: 20rpx;
				font-size: 25rpx;
				color: #FFFFFF;
			}
		}
		.two-data{
			display: flex;
			flex-direction: row;
			align-items: center;
			padding-top: 18rpx;
			.item{
				display: flex;
				flex-direction: column;
				align-items: center;
				font-size: 24rpx;
				line-height: 40rpx;
				width: calc(750rpx/2);
				color: #FFFFFF;
				font-weight: 400;
			}
		}
		.one-data{
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-content: center;
			font-size: 24rpx;
			line-height: 50rpx;
			color: #FFFFFF;
			font-weight: 400;
			padding-top: 10rpx;
		}
	}
	.platform{
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: center;
		height: calc(32rpx * 2 + 116rpx);
		background-color: #FFFFFF;
		image{
			width: 153rpx;
			padding-right: 45rpx;
		}
		.lines{
			.one-line{
				font-size: 30rpx;
				font-family: NotoSansHans;
				font-weight: bold;
				line-height: 40rpx;
				text:first-child{	
					color: #FFBD50;
					padding-right: 15rpx;
				}
				text:last-child{
					color: #424242;
				}
			}
			text:last-child{
				color: #BCBCBC;
				font-size: 22rpx;
			}
		}
	}
	.navs{
		display: flex;
		flex-direction: column;
		height: 220rpx;
		background-color: #FFFFFF;
		margin-top: 10rpx;
		border-bottom: 2rpx solid #F4F1F2;
		padding-bottom: 29rpx;
		text:first-child{
			font-size: 33rpx;
			color: #333333;
			padding-bottom: 45rpx;
			padding-left: 23rpx;
			padding-top: 30rpx;
		}
		.items{
			display: flex;
			flex-direction: row;
			align-items: center;
			justify-content: space-around;
			.item{
				display: flex;
				flex-direction: column;
				align-items: center;
				width: calc(650rpx / 4);
				text{
					font-size: 24rpx;
					color: #555555;
					padding-top: 24rpx;
				}
				image{
					width: 46rpx;
				}
				&:first-child{
					position: relative;
					image:nth-child(2){
						width: 35rpx;
						position: absolute;
						top: -15rpx;
						left: 90rpx;
					}
				}
			}
		}
	}
	.menus{
		display: flex;
		flex-direction: column;
		padding: 0 25rpx;
		background-color: #FFFFFF;
		.item{
			display: flex;
			flex-direction: row;
			align-items: center;
			justify-content: space-between;
			padding: 36rpx 0;
			border-bottom: 2rpx solid #F4F1F2;
			&:active{
				background-color: #F8F8F8;
			}
			image{
				width: 38rpx;
			}
			text{
				font-size: 32rpx;
				font-weight: 400;
				color: #1A191A;
			}
			.left{
				display: flex;
				flex-direction: row;
				align-items: center;
				image{
					padding-right: 28rpx;
				}
			}
			.icon-right{
				font-weight: bold;
				color: #CFCFCF;
				font-size: 27rpx;
			}
		}
	}
</style>
