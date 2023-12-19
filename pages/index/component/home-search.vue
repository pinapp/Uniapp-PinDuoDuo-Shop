<template>
	<view class="search-box">
		<view class="left">
			<image class="search-icon" src="@/static/logo.png"></image>
			<view>男士冬季帽子</view>
		</view>
		<image class="right-icon" src="@/static/logo.png"></image>
	</view>
</template>

<script>
</script>

<style lang="scss" scoped>
	.search-box {
		background-color: #ebedf0;
		padding: 12rpx 24rpx;
		box-sizing: border-box;
		border-radius: 50rpx;
		@include flex-between;
		color: #999;
		width:600rpx;
		.search-icon {
			margin-right: 12rpx;
		}
		.search-icon, .right-icon {
			width: 40rpx;
			height: 40rpx;
		}
		.left {
			flex: 1;
			@include flex-center-center;
		}
	}
</style>