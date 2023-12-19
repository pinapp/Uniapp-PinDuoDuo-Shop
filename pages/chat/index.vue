<style lang="scss">
	page {
		background: #ebedf0;
		min-height: 100vh;
		.list {
			background: #fff;
			.item {
				.right {
					overflow: hidden;
				}
				&::after {
					position: absolute;
					bottom: 0;
					left: 168rpx;
					right: 0;
					height: 1rpx;
					background: darkgray;
					content: "";
					transform: scaleY(.5);
				}
				padding: 24rpx;
				position: relative;
				@include flex-center;
				box-sizing: border-box;
				image {
					width: 120rpx;
					height: 120rpx;
					border-radius: 120rpx;
					margin-right: 24rpx;
					flex: none;
				}
				.top-box, .bottom-box {
					display: flex;
				}
				.top-box {
					@include flex-between;
					align-items: center;
					.title {
						font-size: 36rpx;
						font-weight: bold;
					}
					.time {
						color: darkgray;
						font-size: 28rpx;
					}
				}
				.bottom-box {
					.desc {
						text-overflow: ellipsis;
						overflow: hidden;
						text-wrap: nowrap;
					}
				}
			}
		}
	}
</style>

<template>
	<view class="list">
		<view class="item" v-for="(item, index) in [1,2,3,4,5,6,7,8,9,10,11,12]">
			<image src="/static/logo.png"></image>
			<view class="right">
				<view class="top-box">
					<view class="title">物流助手</view>
					<view class="time">17:57</view>
				</view>
				<view class="bottom-box">
					<view class="desc">亲，这款商品已有60+人好评，品质有保证</view>
					<view class="red">1</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
</script>