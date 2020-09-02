<template>
	<view class="active" :style="{height:this.screenHeight}">
		<view class="header-texts">
			<text>限时领红包</text>
			<text>Each person is limited to 3</text>
		</view>
		<button class="pick-red">我要领红包</button>
		<div class="alert">
			<text>活动规则</text>
			<text>
                                1.活动结束权归设计方所有。
2. 活动结束权归设计方所有，活动结束权归设计方所有，活动结束权归设计方所有
                            </text>
		</div>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				screenHeight: "280px"
			}
		},
		methods: {
			// 动态设置背景高度
			setScreenHeight(){
				new Promise((resolve,reject)=>{
					uni.getSystemInfo({
						success(e) {
							resolve(e)
						}
					})
				}).then(res=>{
					this.screenHeight = res.windowHeight + 'px'
				})
			}
		},
		onLoad() {
			this.setScreenHeight()
		}
	}
</script>

<style lang="scss" scoped>
	.active{
		background-image: url(../../static/active/backgroud.jpg);
		background-repeat: no-repeat;
		background-size: 100%;
		background-color: #F16A33;
	}
	.header-texts{
		display: flex;
		flex-direction: column;
		align-items: center;
		padding-top: 184rpx;
		text:first-child{
			font-size: 98rpx;
			font-weight: bold;
			color: #FFFFFF;
			text-shadow: 0px 9px 6px rgba(194, 83, 56, 0.46);
		}
		text:last-child{
			font-size: 28rpx;
			font-family: NotoSansHans;
			font-weight: bold;
			color: #FFFFFF;
			text-shadow: 0px 5px 1px rgba(194, 83, 56, 0.74);

		}
	}
	.pick-red{
		width: 400rpx;
		height: 80rpx;
		background: linear-gradient(90deg, #FFD632, #FFD338);
		border-radius: 10rpx;
		margin-top: 561rpx;	
		font-size: 32rpx;
		font-family: NotoSansHans;
		font-weight: bold;
		color: #FFFFFF;
		&:active{
			background: linear-gradient(90deg, #D9B63A, #FFD666);
		}
	}
	.alert{
		display: flex;
		flex-direction: column;
		align-items: center;
		text:first-child{
			font-size: 32rpx;
			font-family: NotoSansHans;
			font-weight: 400;
			color: #FFFFFF;
			margin-top: 62rpx;
		}
		text:last-child{
			width: 575rpx;
			font-size: 24rpx;
			font-family: NotoSansHans;
			font-weight: 400;
			color: #FFFFFF;
			text-align: center;
			margin-top: 56rpx;
		}
	}
</style>
