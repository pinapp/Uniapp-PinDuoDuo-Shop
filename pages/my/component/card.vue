<style lang="scss">
	.card {
		:deep .header {
			.title {
				font-size: 36rpx;
				font-weight: bold;
				color: #000;
			}
			.header-right {
				@include flex-center;
				font-size: 24rpx;
				color: darkgray;
				image {
					width: 30rpx;
					height: 30rpx;
					margin-left: 12rpx;
				}
			}
		}
		margin-top: 24rpx;
		background: #fff;
		padding: 32rpx;
		:deep .header {
			@include flex-between;
		}
		:deep .header-right {
			@include flex-center;
		}
		
	}
</style>

<template>
	<view class="card">
		<slot name="header"></slot>
		<slot name="content"></slot>
	</view>
</template>

<script>
</script>