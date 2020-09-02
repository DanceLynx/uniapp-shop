<template>
	<view class="detail">
		<swiper 
			:indicator-dots="true" 
			:autoplay="true" 
			:interval="3000" 
			:duration="1000"
			indicator-color="#CAC8C8"
			indicator-active-color="#FF6252">
			<swiper-item>
				<image src="../../static/shop/swiper-item.jpg" mode="widthFix"></image>
			</swiper-item>
			<swiper-item>
				<image src="../../static/shop/swiper-item.jpg" mode="widthFix"></image>
			</swiper-item>
		</swiper>
		<view class="one">
			<text class="title">暗色运动服春秋棉质流行2019</text>
			<div class="price">
				<view class="two-column">
					<view class="two-row">
						<text>低至八折</text>
						<text>全新上市</text>
					</view>
					<text class="price">￥599.00</text>
				</view>
				<view class="share">
					<image src="../../static/shop/icon-5.png" mode="widthFix"></image>
					<text>分享有奖</text>
				</view>
			</div>
		</view>
		<view class="wish-bar">
			<view class="item">
				<image src="../../static/shop/icon-2.png" mode="widthFix"></image>
				<text>正品保障</text>
			</view>
			<view class="item">
				<image src="../../static/shop/icon-3.png" mode="widthFix"></image>
				<text>自营销售</text>
			</view>
			<view class="item">
				<image src="../../static/shop/icon-1.png" mode="widthFix"></image>
				<text>假一赔十</text>
			</view>
			<view class="item">
				<image src="../../static/shop/icon-2.png" mode="widthFix"></image>
				<text>售后无忧</text>
			</view>
		</view>
		<view class="discount">
			<text>优惠活动</text>
			<view class="items">
				<text>满200减10</text>
				<text>满300减20</text>
			</view>
		</view>
		<view class="shop">
			<view class="user">
				<image src="../../static/my/icon-11.png" mode="widthFix"></image>
				<view class="items">
					<text>服饰店铺</text>
					<text>已经过认证</text>
				</view>
			</view>
			<view class="in-shop">
				<text>进入店铺</text>
				<i class="iconfont icon-right"></i>
			</view>
		</view>
		<view class="shop-content">
			<text>商品详情</text>
		</view>
		<view class="shop-bar">
			<view class="left">
				<view class="item">
					<image src="../../static/shop/zan.png" mode="widthFix"></image>
					<text>收藏</text>
				</view>
				<view class="item">
					<image src="../../static/shop/message.png" mode="widthFix"></image>
					<text>评论</text>
				</view>
			</view>
			<view class="right">
				<button>加入购物车</button>
				<button>立即购买</button>
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
	swiper{
		width: 750rpx;
		height: calc(473rpx + 19rpx * 2);
		image{
			width: 750rpx;
		}
	}
	.one{
		width: 700rpx;
		padding: 0rpx 25rpx;
		height: 190rpx;
		background-color: #FFFFFF;
		.title{
			font-size: 36rpx;
			font-weight: 400;
			color: #515151;
			margin-bottom: 15rpx;
		}
		.price{
			display: flex;
			flex-direction: row;
			align-items: center;
			justify-content: space-between;
			.two-column{
				display: flex;
				flex-direction: column;
				.two-row{
					display: flex;
					flex-direction: row;
					text{
						width: 108rpx;
						font-size: 24rpx;
						color: #BFBFBF;
						display: block;
					}
					text:last-child{
						margin-left: 21rpx;
						border-left: 5rpx solid #FF6252;
						padding-left: 22rpx;
					}
				}
				text.price{
					font-size: 37rpx;
					color: #FF3133;
					margin-top: 36rpx;
					padding-left: 8rpx;
				}
			}
			.share{
				display: flex;
				flex-direction: column;
				align-items: center;
				height: 77rpx;
				text{
					font-size: 25rpx;
					color: #BBBBBB;
					margin-top: 19rpx;
				}
				image{
					width: 38rpx;
				}
			}
		}
	}
	.wish-bar{
		width: 750rpx;
		height: 107rpx;
		background-color: #FFF6F7;
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: space-between;
		.item{
			display: flex;
			flex-direction: row;
			justify-content: center;
			align-items: center;
			width: calc(750rpx / 4);
			image{
				width: 24rpx;
			}
			text{
				font-size: 25rpx;
				color: #B2B2B2;
				margin-left: 14rpx;
			}
		}
	}
	.discount{
		width: 700rpx;
		height: 96rpx;
		padding: 0 25rpx;
		display: flex;
		flex-direction: row;
		align-items: center;
		background-color: #FFFFFF;
		border-bottom: 3rpx solid #F3F3F3;
		& > text:first-child{
			font-size: 30rpx;
			color: #525252;
			font-weight: 400;
		}
		.items{
			font-size: 24rpx;
			color: #AEAEAE;
			margin-left: 69rpx;
			text:last-child{
				margin-left: 35rpx;
			}
		}
	}
	.shop{
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: space-between;
		width: 750rpx;
		height: 157rpx;
		background-color: #FFFFFF;
		.user{
			display: flex;
			flex-direction: row;
			align-items: center;
			image{
				width: 85rpx;
				border-radius: 50%;
				background-color: #FAFBFD;
				margin-right: 19rpx;
			}
			.items{
				display: flex;
				flex-direction: column;
				text:first-child{
					font-size: 31rpx;
					font-weight: 400;
					color: #2D2D2D;
				}
				text:last-child{
					font-size: 24rpx;
					color: #B6B6B6;
					margin-top: 18rpx;
				}
			}	
		}
		.in-shop{
			text{
				font-size: 31rpx;
				color: #EC6866;
				font-weight: 400;
			}
			i{
				font-size: 31rpx;
				color: #EC6866;
				margin-left: 22rpx;
			}
		}
	}
	.shop-content{
		background-color: #FFFFFF;
		margin-top: 10rpx;
		border-radius: 10rpx;
		height: 1000rpx;
		margin-bottom: 86rpx;
	}
	.shop-bar{
		display: flex;
		flex-direction: row;
		height: 86rpx;
		align-items: center;
		justify-content: space-between;
		background-color: #FFEEEE;
		position: fixed;
		bottom: 0rpx;
		left: 0rpx;
		right: 0rpx;
		.left{
			display: flex;
			flex-direction: row;
			align-items: center;
			.item{
				display: flex;
				flex-direction: row;
				align-items: center;
				&:first-child{
					margin-right: 65rpx;
					padding-left: 29rpx;
				}
				image{
					width: 28rpx;
				}
				text{
					font-size: 22rpx;
					font-weight: 400;
					color: #7B7B7B;
					margin-left: 26rpx;
				}
			}
		}
		.right{
			display: flex;
			flex-direction: row;
			align-items: center;
			button{
				height: 86rpx;
				line-height: 86rpx;
				width: 180rpx;
				border-radius: 0rpx;
				font-size: 26rpx;
				color: #FFFFFF;
				border: none;
				&:first-child{
					background-color: #FFBB36;
				}
				&:last-child{
					background: linear-gradient(90deg, #FF6252, #FF9E56);
				}
			}
		}
	}
</style>
