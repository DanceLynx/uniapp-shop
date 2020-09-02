<template>
	<view class="cart">
		<view class="list">
			<block v-for="item,index in list" :key="index">
				<view class="item">
					<image 
						src="../../static/cart/Btn_select_per.png" 
						mode="widthFix"
						v-show="item.selected == 1"
						@tap="changeSelect(index,0)"></image>
					<image
						src="../../static/cart/Btn_select.png" 
						mode="widthFix"
						v-show="item.selected == 0"
						@tap="changeSelect(index,1)"></image>
					<image src="../../static/shop/swiper-item.jpg" mode="widthFix"></image>
					<view class="content">
						<view>
							<text>{{item.title}}</text>
						</view>
						<view>
							<text>颜色分类：暗色</text>
							<text>尺码：190</text>
						</view>
						<view class="specs">
							<view class="price">
								<text>￥299.00</text>
								<text>￥399.00</text>
							</view>
							<view class="numbers">
								<text @tap="changeCount(index,'minus')">-</text>
								<text>{{item.count}}</text>
								<text @tap="changeCount(index)">+</text>
							</view>
						</view>
					</view>
				</view>
			</block>			
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list:[
					{
						"title":"[暗色卫衣]运动系列条纹暗色秋春卫衣",
						"selected":1,
						"count":1
					},
					{
						"title":"[暗色卫衣]运动系列条纹暗色秋春卫衣",
						"selected":0,
						"count":1
					},
					{
						"title":"[暗色卫衣]运动系列条纹暗色秋春卫衣",
						"selected":0,
						"count":1
					}
				]
			}
		},
		methods: {
			changeSelect(index,is_selected){
				this.list[index].selected = is_selected;
			},
			changeCount(index,option="add"){
				if(option == 'add')
					this.list[index].count++
				if(option == 'minus' && this.list[index].count > 0)
					this.list[index].count--
			}
		}
	}
</script>

<style lang="scss" scoped>
	.item{
		width: 750rpx;
		height: 276rpx;
		display: flex;
		flex-direction: row;
		align-items: center;
		background-color: #FFFFFF;
		justify-content: space-around;
		margin-bottom: 17rpx;
		image:nth-of-type(1),image:nth-of-type(2){
			width: 36rpx;
		}
		image:nth-of-type(3){
			width: 219rpx;
		}
		.content{
			display: flex;
			flex-direction: column;
			&>view:nth-of-type(1){
				font-size: 28rpx;
				width: 278rpx;
				color: #333333;
				font-weight: 400;
			}
			&>view:nth-of-type(2){
				font-size: 20rpx;
				color: #666666;
				font-weight: 400;
				margin-top: 21rpx;
				text:first-child{
					margin-right: 16rpx;
				}
			}
			.specs{
				display: flex;
				align-items: flex-end;
				justify-content: space-between;
				width: 350rpx;
				margin-top: 20rpx;
				.price{
					display: flex;
					flex-direction: column;
					text:first-child{
						font-size: 28rpx;
						font-weight: 400;
						color: #FF6252;
					}
					text:last-child{
						font-size: 28rpx;
						font-weight: 400;
						color: #333333;
						text-decoration: line-through;
					}
				}
				.numbers{
					display: flex;
					align-items: center;
					text:nth-of-type(2){
						font-size: 25rpx;
						font-weight: 400;
						margin: 0 30rpx;
					}
					text:first-child,text:last-child{
						width: 39rpx;
						height: 39rpx;
						line-height: 39rpx;
						text-align: center;
						font-size: 35rpx;
						font-weight: bold;
						border: 1rpx solid #666666;
						border-radius: 4rpx;
					}
				}
			}
		}
	}
</style>
