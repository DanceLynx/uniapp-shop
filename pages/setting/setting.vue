<template>
	<view class="setting">
		<view class="items">
			<view class="item">
				<text>账号管理</text>
				<i class="iconfont icon-right"></i>
			</view>
			<view class="item">
				<text>账号与安全</text>
				<i class="iconfont icon-right"></i>
			</view>
		</view>
		
		<view class="items">
			<view class="item">
				<text>消息设置</text>
				<i class="iconfont icon-right"></i>
			</view>
			<view class="item">
				<text>隐私设置</text>
				<i class="iconfont icon-right"></i>
			</view>
			<view class="item">
				<text>通用设置</text>
				<i class="iconfont icon-right"></i>
			</view>
			<view class="item">
				<text>地图设置</text>
				<i class="iconfont icon-right"></i>
			</view>
			<view class="item">
				<text>接受推送</text>
				<view class="switch">
					<switch checked="true" color="#FF6251" />
				</view>
			</view>
		</view>
		
		<view class="items">
			<view class="item">
				<text>关于我们</text>
				<i class="iconfont icon-right"></i>
			</view>
			<view class="item">
				<text>清除缓存</text>
				<i class="iconfont icon-right"></i>
			</view>
		</view>
		
		<view class="button">
			<button>退出</button>
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
	.items{
		width: 700rpx;
		padding: 0 25rpx;
		display: flex;
		flex-direction: column;
		margin-top: 20rpx;
		background-color: #FFFFFF;
		.item{
			display: flex;
			height: 100rpx;
			align-items: center;
			justify-content: space-between;
			font-size: 30rpx;
			font-weight: 400;
			color: #333333;
			i{
				font-size: 15rpx;
				color: #999999;
			}
			view.switch{
				width: 90rpx;
				switch{
					transform: scale(0.6);
				}
			}
		}
	}
	.button{
		width: 750rpx;
		margin-top: 62rpx;
		button{
			width: 492rpx;
			height: 81rpx;
			background: linear-gradient(90deg, #FF6251, #FF9D55);
			border-radius: 41rpx;
			color: #FFFFFF;
			font-size: 36rpx;
			line-height: 81rpx;
		}
	}
</style>
