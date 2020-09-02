<template>
	<view class="confirm">
		<view class="address">
			<image src="../../static/order/icon-1.png" mode="widthFix"></image>
			<view class="content">
				<text class="title">中国浙江省杭州市西湖区88号</text>
				<text class="name">王二 (收)</text>
				<text class="alert">(收货不便时，可以选择免费代收服务)</text>
			</view>
		</view>
		<image src="../../static/order/bar.png" mode="widthFix" class="colorful-bar"></image>
		<view class="center">
			<div class="shop">
				<image src="../../static/order/left.jpg" mode="widthFix"></image>
				<view class="texts">
					<view class="title">
						<text>晴雨两用伞-下雨天和晴天都能用</text>
					</view>
					<view class="specs">
						<text>￥99.00</text>
						<text>x1</text>
					</view>
				</view>
			</div>
		</view>
		<view class="seven-day">
			<text>商品支持7天无理由退货</text>
		</view>
		<view class="distribution">
			<text>配送方式</text>
			<text>包邮</text>
		</view>
		<view class="message">
			<text>买家留言</text>
			<input type="text" value="" placeholder="买家留言买家留言" />
		</view>
		<view class="price-specs">
			<text>共1件商品</text>
			<text>共计：</text>
			<text>99.00</text>
		</view>
		<view class="integral">
			<text>用积分抵扣</text>
			<view>
				<switch checked="true" color="#FF6252"  />
			</view>	
		</view>
		<view class="bottom-bar">
			<text>共计金额：</text>
			<text>99.00</text>
			<view>
				<button>提交订单</button>
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
	.colorful-bar{
		width: 750rpx;
		position: absolute;
		top: 189rpx;
	}
	.address{
		width: 700rpx;
		padding: 0 25rpx;
		display: flex;
		flex-direction: row;
		align-items: center;
		height: 184rpx;
		margin-top: 3rpx;
		background-color: #FFFFFF;
		&>image{
			margin-right: 28rpx;
			width: 36rpx;
		}
		.content{
			display: flex;
			flex-direction: column;
			font-size: 28rpx;
			color: #343434;
			font-weight: 400;
			.alert{
				color: #FF6252;
				font-size: 24rpx;
			}
		}
	}
	.center{
		width: 700rpx;
		padding: 0 25rpx;
		display: flex;
		margin-top: 11rpx;
		background-color: #FFFFFF;
		.shop{
			display: flex;
			align-items: center;
			height: 207rpx;
			image{
				width: 206rpx;
				margin-right: 24rpx;
			}
			.texts{
				display: flex;
				flex-direction: column;
				justify-content: space-between;
				height: 150rpx;
				width: calc(334rpx + 120rpx);
				.title{
					width: 380rpx;
					text{
						font-size: 28rpx;
						color: #343434;
						font-weight: 400;
					}
				}
				.specs{
					display: flex;
					justify-content: space-between;
					align-items: flex-end;
					text:first-child{
						font-size: 36rpx;
						font-weight: 400;
						color: #E6423A;
					}
					text:last-child{
						font-size: 24rpx;
						color: #666666;
						font-weight: 400;
					}
				}
			}
		}
	}
	.seven-day{
		width: 700rpx;
		height: 90rpx;
		padding: 0 25rpx;
		background-color: #FFFFFF;
		text{
			font-size: 28rpx;
			font-weight: 400;
			color: #343434;
			line-height: 90rpx;
		}
	}
	.distribution{
		width: 700rpx;
		padding: 0 25rpx;
		background-color: #FFFFFF;
		height: 90rpx;
		display: flex;
		justify-content: space-between;
		align-items: center;
		border-top: 2rpx solid #F0F0F0;
		text{
			font-size: 28rpx;
			font-weight: 400;
			color: #343434;
		}
	}
	.message{
		width: 700rpx;
		padding: 0 25rpx;
		background-color: #FFFFFF;
		height: 90rpx;
		display: flex;
		align-items: center;
		border-top: 2rpx solid #F0F0F0;
		text{
			font-size: 28rpx;
			font-weight: 400;
			color: #343434;
			margin-right: 20rpx;
		}
		input{
			font-size: 28rpx;
		}
	}
	.price-specs{
		width: 700rpx;
		padding: 0 25rpx;
		background-color: #FFFFFF;
		height: 90rpx;
		display: flex;
		align-items: center;
		justify-content: flex-end;
		border-top: 2rpx solid #F0F0F0;
		text{
			font-size: 28rpx;
			font-weight: 400;
			color: #343434;
		}
		text:first-child{
			margin-right: 15rpx;
		}
		text:last-child{
			color: #FF7A54;
		}
	}
	.integral{
		width: 700rpx;
		padding: 0 25rpx;
		height: 90rpx;
		margin-top: 20rpx;
		background-color: #FFFFFF;
		display: flex;
		align-items: center;
		justify-content: space-between;
		text{
			font-size: 28rpx;
			font-weight: 400;
			color: #343434;
		}
		view{
			width: 90rpx;
			switch{
				transform: scale(0.6); 
			}
		}
	}
	.bottom-bar{
		width: 750rpx;
		height: 90rpx;
		background-color: #FFFFFF;
		display: flex;
		// align-items: center;
		flex-direction: row;
		justify-content: flex-end;
		position: fixed;
		bottom: 0rpx;
		left: 0rpx;
		right: 0rpx;
		align-items: center;
		text:first-child{
			font-size: 28rpx;
			font-weight: 400;
			color: #333333;
		}
		text:nth-of-type(2){
			font-size: 36rpx;
			font-weight: 400;
			color: #FF7252;
		}
		view{
			margin-left: 58rpx;
			button{
				width: 190rpx;
				height: 90rpx;
				color: #FEFEFE;
				font-size: 28rpx;
				line-height: 90rpx;
				background: linear-gradient(90deg, #FF6251, #FF9D55);
				background-color: #4CD964;
				border-radius: 0rpx;
			}
		}
	}
</style>
