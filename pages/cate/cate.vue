<template>
	<view class="cate">
		<view class="left">
			<view class="item" :class="{active: leftIndex == 0}" @tap="leftIndex = 0">
				<text>为您推荐</text>
			</view>
			<view class="item" :class="{active: leftIndex == 1}" @tap="leftIndex = 1">
				<text>内衣配饰</text>
			</view>
			<view class="item" :class="{active: leftIndex == 2}" @tap="leftIndex = 2">
				<text>珠宝配饰</text>
			</view>
			<view class="item" :class="{active: leftIndex == 3}" @tap="leftIndex = 3">
				<text>户外运动</text>
			</view>
			<view class="item" :class="{active: leftIndex == 4}" @tap="leftIndex = 4">
				<text>女装</text>
			</view>
			<view class="item" :class="{active: leftIndex == 5}" @tap="leftIndex = 5">
				<text>家装</text>
			</view>
			<view class="item" :class="{active: leftIndex == 6}" @tap="leftIndex = 6">
				<text>鞋靴</text>
			</view>
		</view>
		<view class="right">
			<view class="box" :style="{display:leftIndex==0?'flex':'none'}">
				<text class="one">排行榜</text>
				<image src="../../static/cate/viewMore.jpg" mode="widthFix"></image>
				<text class="one">热门推荐</text>
				<view class="content">
					<view class="item">
						<image src="../../static/cate/cate-1.jpg" mode="widthFix"></image>
						<text>男鞋</text>
					</view>
					<view class="item">
						<image src="../../static/cate/cate-2.jpg" mode="widthFix"></image>
						<text>跑步鞋</text>
					</view>
					<view class="item">
						<image src="../../static/cate/cate-2.jpg" mode="widthFix"></image>
						<text>跑步鞋</text>
					</view>
					<view class="item">
						<image src="../../static/cate/cate-1.jpg" mode="widthFix"></image>
						<text>男鞋</text>
					</view>
					<view class="item">
						<image src="../../static/cate/cate-2.jpg" mode="widthFix"></image>
						<text>跑步鞋</text>
					</view>
					<view class="item">
						<image src="../../static/cate/cate-2.jpg" mode="widthFix"></image>
						<text>跑步鞋</text>
					</view>
					<view class="item">
						<image src="../../static/cate/cate-1.jpg" mode="widthFix"></image>
						<text>男鞋</text>
					</view>
					<view class="item">
						<image src="../../static/cate/cate-2.jpg" mode="widthFix"></image>
						<text>跑步鞋</text>
					</view>
					<view class="item">
						<image src="../../static/cate/cate-2.jpg" mode="widthFix"></image>
						<text>跑步鞋</text>
					</view>
				</view>
			</view>
			<view class="box" :style="{display:leftIndex==1?'flex':'none'}">
				<text>内衣服饰</text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				leftIndex: 0
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss" scoped>
	.cate{
		display: flex;
		flex-direction: row;
	}
	.left{
		display: flex;
		flex-direction: column;
		width: 160rpx;
		height: fit-content;
		position: fixed;
		top: 0rpx;
		border: none;
		background-color: #FFFFFF;
		text-align: center;
		.item{
			padding: 34rpx 0;
			font-size: 28rpx;
			color: #333333;
			text{
				width: 160rpx;
				display: block;
			}
		}
		.active{
			background-color: $background-color;
			color: #F87026;
			text{
				width: 154rpx;
				border-left: 6rpx solid #FF6251;
			}
		}
	}
	.right{
		display: flex;
		flex-direction: column;
		padding: 0 22rpx;
		margin-left: 160rpx;
		.box{
			display: flex;
			flex-direction: column;
			.one{
				font-size: 28rpx;
				color: #333333;
				font-weight: 400;
				padding-bottom: 31rpx;
				&:first-child{
					padding-top: 32rpx;
				}
			}
			& > image{
				width: 544rpx;
				padding-bottom: 51rpx;
			}
			.content{
				width: 544rpx;
				background-color: #FFFFFF;
				height: 637rpx;
				border-radius: 10rpx;
				display: flex;
				flex-direction: row;
				flex-wrap: wrap;
				align-items: center;
				padding: 10rpx 0;
				.item{
					display: flex;
					flex-direction: column;
					align-items: center;
					width: calc(544rpx / 3);
					font-size: 24rpx;
					color: #666666;
					image{
						width: 110rpx;
						margin-bottom: 14rpx;
					}
				}
			}
		}
	}
</style>
