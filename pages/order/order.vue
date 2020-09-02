<template>
	<view class="order">
		<view class="header-bar">
			<view class="item" :class="{'active':currentBarIndex == 0}" @tap="currentBarIndex = 0">全部</view>
			<view class="item" :class="{'active':currentBarIndex == 1}" @tap="currentBarIndex = 1">待付款</view>
			<view class="item" :class="{'active':currentBarIndex == 2}" @tap="currentBarIndex = 2">待收货</view>
			<view class="item" :class="{'active':currentBarIndex == 3}" @tap="currentBarIndex = 3">已收货</view>
			<view class="item" :class="{'active':currentBarIndex == 4}" @tap="currentBarIndex = 4">未完成</view>
		</view>
		<view class="order-list" :style="{display:currentBarIndex == 0 ? 'block':'none'}">
			<view class="item">
				<text>卫衣旗舰店</text>
				<view class="content">
					<image src="../../static/shop/swiper-item.jpg" mode="widthFix"></image>
					<view class="right">
						<text>秋冬卫衣暗色运动跑步</text>
						<text>x1</text>
						<text>颜色：白色  尺码：M</text>
						<view class="price">
							<text>￥299.00</text>
							<text>￥499.00</text>
							<text>x1</text>
						</view>
					</view>
				</view>
				<view class="number">
					<text>共1件商品</text>
					<text>合计：</text>
					<text>￥299.00</text>
				</view>
				<view class="button">
					<button>查看物流</button>
				</view>
			</view>
			<view class="item">
				<text>卫衣旗舰店</text>
				<view class="content">
					<image src="../../static/shop/swiper-item.jpg" mode="widthFix"></image>
					<view class="right">
						<text>秋冬卫衣暗色运动跑步</text>
						<text>x1</text>
						<text>颜色：白色  尺码：M</text>
						<view class="price">
							<text>￥299.00</text>
							<text>￥499.00</text>
							<text>x1</text>
						</view>
					</view>
				</view>
				<view class="number">
					<text>共1件商品</text>
					<text>合计：</text>
					<text>￥299.00</text>
				</view>
				<view class="button">
					<button>查看物流</button>
				</view>
			</view>
		</view>
		<view class="order-list" :style="{display:currentBarIndex == 1 ? 'block':'none'}">
			<view class="item">
				<text>卫衣旗舰店</text>
				<view class="content">
					<image src="../../static/shop/swiper-item.jpg" mode="widthFix"></image>
					<view class="right">
						<text>秋冬卫衣暗色运动跑步</text>
						<text>x1</text>
						<text>颜色：白色  尺码：M</text>
						<view class="price">
							<text>￥299.00</text>
							<text>￥499.00</text>
							<text>x1</text>
						</view>
					</view>
				</view>
				<view class="number">
					<text>共1件商品</text>
					<text>合计：</text>
					<text>￥299.00</text>
				</view>
				<view class="button">
					<button>立即付款</button>
				</view>
			</view>
			<view class="item">
				<text>卫衣旗舰店</text>
				<view class="content">
					<image src="../../static/shop/swiper-item.jpg" mode="widthFix"></image>
					<view class="right">
						<text>秋冬卫衣暗色运动跑步</text>
						<text>x1</text>
						<text>颜色：白色  尺码：M</text>
						<view class="price">
							<text>￥299.00</text>
							<text>￥499.00</text>
							<text>x1</text>
						</view>
					</view>
				</view>
				<view class="number">
					<text>共1件商品</text>
					<text>合计：</text>
					<text>￥299.00</text>
				</view>
				<view class="button">
					<button>立即付款</button>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				currentBarIndex:0
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss" scoped>
	.header-bar{
		width: 700rpx;
		padding: 0 25rpx;
		height: 89rpx;
		display: flex;
		align-items: center;
		background-color: #FFFFFF;
		.item{
			width: calc(700rpx / 5);
			height: 89rpx;
			line-height: 89rpx;
			font-size: 28rpx;
			font-weight: 400;
			color: #525252;
			text-align: center;
		}
		.active{
			color: #16BA64;
			background: linear-gradient(0deg, #FF6252 0%, #FF9E56 100%);
			-webkit-background-clip: text;
			-webkit-text-fill-color: transparent;
			border-bottom: 3rpx solid #FF6252;
		}
	}
	.order-list{
		width: calc(750rpx - 27rpx * 2);
		padding: 0rpx 27rpx;
		.item{
			display: flex;
			flex-direction: column;
			padding: 28rpx 31rpx;
			width: calc(750rpx - 27rpx * 2 + 31 * 2);
			margin-top: 18rpx;
			// height: calc(516rpx - 28rpx * 2);
			background-color: #FFFFFF;
			border-radius: 21rpx;
			&>text:first-child{
				font-size: 28rpx;
				font-weight: 400;
				color: #FF6252;
				padding-bottom: 30rpx;
				border-bottom: 2rpx solid #EFEFEF;
			}
			.content{
				display: flex;
				align-items: center;
				margin-left: 14rpx;
				margin-top: 31rpx;
				border-bottom: 2rpx solid #EFEFEF;
				padding-bottom: 31rpx;
				.right{
					display: flex;
					flex-direction: column;
					margin-left: 40rpx;
					&>text:first-child,&>text:nth-of-type(2){
						font-size: 26rpx;
						font-weight: 400;
						color: #4E4E4E;
					}
					&>text:nth-of-type(3){
						margin-top: 38rpx;
						font-size: 23rpx;
						font-weight: 400;
						color: #7E7E7E;
					}
					.price{
						display: flex;
						margin-top: 40rpx;
						align-items: flex-end;
						text:first-child{
							font-size: 29rpx;
							font-weight: 400;
							color: #4D4D4D;
						}
						text:nth-of-type(2),text:nth-of-type(3){
							font-size: 22rpx;
							font-weight: 400;
							color: #949494;
							margin-left: 10rpx;
							text-decoration: line-through;
						}
						text:nth-of-type(3){
							text-decoration: none;
						}
					}
				}
				image{
					width: 149rpx;
				}
			}
			.number{
				display: flex;
				align-self: flex-end;
				font-size: 26rpx;
				color: #535353;
				align-items: flex-end;
				margin-top: 63rpx;
				font-weight: 400;
				text:nth-of-type(3){
					font-size: 29rpx;
				}
			}
			.button{
				display: flex;
				align-self: flex-end;
				margin-top: 31rpx;
				button{
					width: 159rpx;
					height: 63rpx;
					line-height: 63rpx;
					font-size: 24rpx;
					font-weight: 400;
					color: #FFFFFF;
					background: linear-gradient(90deg, #FF6252, #FF9E56);
					border-radius: calc(63rpx / 2);
				}
			}
		}
	}
</style>
