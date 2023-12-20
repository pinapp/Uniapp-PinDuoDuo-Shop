<style lang="scss" scoped>
	.list {
		maring-top: 24rpx;
		:deep .uni-scroll-view-content {
			@include flex-center;
			flex-wrap: wrap;
			box-sizing: border-box;
			padding-left: 24rpx;
			padding-top: 24rpx;
			justify-content: space-between;
		}
		.item {
			width: 50%;
			margin-bottom: 24rpx;
			box-sizing: border-box;
			padding-right: 24rpx;
			.content {
				border-radius: 12rpx;
				background-color: #fff;
			}
			image {
				width: 100%;
				height: 50vw;
			}
			.row {
				@include flex-center;
			}
			.base {
				padding: 4rpx 18rpx 8rpx;
				.title {
					font-size: 36rpx;
					font-weight: 500;
				}
				.use {
					@include flex-center;
					padding-top: 8rpx;
					image {
						width: 30rpx;
						height: 30rpx;
						margin-right: 8rpx;
					}
					.title {
						color: limegreen;
						font-size: 28rpx;
					}
				}
			}
			.low {
				font-size: 28rpx;
				margin-left: 12rpx;
				color: orangered;
				font-weight: 500;
			}
			
			.sale-box {
				padding-top: 8rpx;
				padding-bottom: 12rpx;
				.price {
					color: orangered;
					font-weight: bold;
					font-size: 32rpx;
				}
				
				.sale {
					font-size: 24rpx;
					color: darkgray;
					margin-left: 12rpx;
				}
			}
		}
	}
</style>

<template>
	<scroll-view class="list" scroll-y>
		<view class="item" v-for="(item,index) in [1,2,3,4,5,6,7,8,9,10]">
			<view class="content">
				<image src="@/static/logo.png"></image>
				<view class="base">
					<view class="title">少女法式小吊带</view>
					<view class="row">
						<view class="use">
							<image src="@/static/logo.png"></image>
							<view class="title">先用后付</view>
						</view>
						<view class="low">30天低价</view>
					</view>
					<view class="row sale-box">
						<view class="price">￥10.49</view>
						<view class="sale">已拼3100件</view>
					</view>
				</view>
			</view>
		</view>
	</scroll-view>
</template>

<script>
	export default {
		data() {
			return {}
		}
	}
</script>

