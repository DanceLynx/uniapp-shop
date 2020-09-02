<template>
	<view class="index">
		<swiper 
			:indicator-dots="false" 
			:autoplay="true" 
			:interval="3000" 
			:duration="1000" 
			class="banner">
			<swiper-item>
				<image src="../../static/home/banner.jpg" mode="widthFix"></image>
			</swiper-item>
			<swiper-item>
				<image src="../../static/home/banner.jpg" mode="widthFix"></image>
			</swiper-item>
		</swiper>
		<swiper :indicator-dots="true" 
			:autoplay="false" 
			:duration="300"
			indicator-active-color="#F74F70"
			indicator-color="#BFB5B7"
			class="grid-menu">
			<swiper-item>
				<view class="item">
					<image src="../../static/home/icon-1.png" mode="widthFix"></image>
					<text>公告</text>
				</view>
				<view class="item">
					<image src="../../static/home/icon-5.png" mode="widthFix"></image>
					<text>酒店</text>
				</view>
				<view class="item">
					<image src="../../static/home/icon-4.png" mode="widthFix"></image>
					<text>购物车</text>
				</view>
				<view class="item">
					<image src="../../static/home/icon-1.png" mode="widthFix"></image>
					<text>公告</text>
				</view>
				<view class="item">
					<image src="../../static/home/icon-3.png" mode="widthFix"></image>
					<text>活动</text>
				</view>
				<view class="item">
					<image src="../../static/home/icon-2.png" mode="widthFix"></image>
					<text>旅游</text>
				</view>
				<view class="item">
					<image src="../../static/home/icon-6.png" mode="widthFix"></image>
					<text>饮料</text>
				</view>
				<view class="item">
					<image src="../../static/home/icon-6.png" mode="widthFix"></image>
					<text>饮料</text>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="item">
					<image src="../../static/home/icon-1.png" mode="widthFix"></image>
					<text>公告</text>
				</view>
				<view class="item">
					<image src="../../static/home/icon-5.png" mode="widthFix"></image>
					<text>酒店</text>
				</view>
				<view class="item">
					<image src="../../static/home/icon-4.png" mode="widthFix"></image>
					<text>购物车</text>
				</view>
				<view class="item">
					<image src="../../static/home/icon-3.png" mode="widthFix"></image>
					<text>活动</text>
				</view>
				<view class="item">
					<image src="../../static/home/icon-2.png" mode="widthFix"></image>
					<text>旅游</text>
				</view>
				<view class="item">
					<image src="../../static/home/icon-6.png" mode="widthFix"></image>
					<text>饮料</text>
				</view>
				<view class="item">
					<image src="../../static/home/icon-6.png" mode="widthFix"></image>
					<text>饮料</text>
				</view>
			</swiper-item>
		</swiper>
		<view class="hot-bar">
			<text class="hot-text">热门推荐</text>
			<text class="alert-text">一些进口零食 限时促销啦</text>
			<i class="iconfont icon-gengduo"></i>
		</view>
		<view class="hot-area">
			<view class="content">
				<image src="../../static/home/banner1.jpg" mode="widthFix"></image>
				<view class="items">
					<view class="item">
						<text class="title">休闲零食</text>
						<text class="info">最低30</text>
					</view>
					<view class="item">
						<text class="title">新鲜水果</text>
						<text class="info">活动特价9.9元</text>
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
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss" scoped>
	.banner{
		width: 750rpx;
		height: 384rpx;
		image{
			width: 100%;
		}
	}
	.grid-menu{
		width: 750rpx;
		height: 374rpx;
		background-color: #FFFFFF;
		border-radius: 12rpx;
		swiper-item{
			display: flex;
			flex-direction: row;
			align-items: center;
			flex-wrap: wrap;
			.item{
				display: flex;
				flex-direction: column;
				align-items: center;
				width: 187.5rpx;
				font-size: 24rpx;
				padding: 30rpx 0;
				color: #767676;
				image{
					width: 72rpx;
					height: 72rpx;
				}
				text{
					padding-top: 14rpx;
				}
			}
		}
	}
	.hot-bar{
		width: 750rpx;
		height: 80rpx;
		margin-top: 7rpx;
		background-color: #FFFFFF;
		border-radius: 12rpx;
		display: flex;
		flex-direction: row;
		justify-content: space-around;
		align-items: center;
		.hot-text{
			width: 130rpx;
			font-size: 31rpx;
			font-weight: 400;
			background-color: red;
			color: #2ECBC2;
			background: linear-gradient(0deg, #FF6251 0%, #FF9D55 100%);
			-webkit-background-clip: text;
			-webkit-text-fill-color: transparent;
		}
		.alert-text{
			width: 450rpx;
			font-size: 24rpx;
			font-family: NotoSansHans;
			font-weight: 400;
			color: #3F3F3F;

		}
		i{
			font-size: 70rpx;
			color: #D6D7DC;
		}
	}
	.hot-area{
		width: 750rpx;
		height: 400rpx;
		margin-top: 7rpx;
		border-radius: 12rpx;
		background-color: #FFFFFF;
		.content{
			width: 700rpx;
			padding: 0 25rpx;
			padding-top: 30rpx;
			border-radius: 6rpx;
			border: 1rpx solid #DBDCE0;
			.items{
				display: flex;
				flex-direction: row;
				padding: 0 21rpx;
				.item{
					width: 290rpx;
					display: flex;
					flex-direction: column;
					margin-top: 20rpx;
					padding: 0 9.75rpx;
					&:first-child{
						border-right: 1rpx solid #DBDCE0;
					}
					.title{
						width: 111rpx;
						font-size: 28rpx;
						font-family: NotoSansHans;
						font-weight: 400;
						color: #DB0C14;
						margin-bottom: 13rpx;
						background: linear-gradient(0deg, #FF6251 0%, #FF9D55 100%);
						-webkit-background-clip: text;
						-webkit-text-fill-color: transparent;

					}
					.info{
						width: 200rpx;
						font-size: 22rpx;
						font-family: NotoSansHans;
						font-weight: 400;
						color: #7F8699;
					}
				}
			}
			image{
				width: 100%;
			}
		}
	}
</style>
