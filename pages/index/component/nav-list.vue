<template>
	<view class="active-box">
		<view class="left">
			<image src="@/static/logo.png"></image>
			<view class="title">百亿补贴</view>
			<view class="desc">大牌正品</view>
		</view>
		<view class="right">
			<view class="item" v-for="(item, index) in [1,2,3,4]">
				<image src="@/static/logo.png"></image>
				<view class="price">￥1.99</view>
			</view>
		</view>
	</view>
</template>

<style lang="scss" scoped>
	// 活动
	.active-box {
		@include flex-center;
		margin-top: 24rpx;
		background: #fff;
		padding: 24rpx;
		.left {
			display: flex;
			flex-direction: column;
			justify-content: center;
			width: fit-content;
			align-items: center;
			margin-right: 24rpx;
			image {
				width: 80rpx;
				height: 80rpx;
			}
			.title {
				font-size: 34rpx;
				color: #000;
				margin-top: 12rpx;
			}
			.desc {
				color: #999;
				font-size: 28rpx;
			}
		}
		
		.right {
			display: flex;
			flex: 1;
			.item {
				text-align: center;
				flex: 1;
				image {
					width: 120rpx;
					height: 120rpx;
				}
				.price {
					color: red;
					font-size: 32rpx;
					font-weight: bold;
				}
			}
		}
	}
</style>