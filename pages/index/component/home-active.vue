<template>
	<view class="nav-list">
		<view class="item" v-for="(item, index) in [1,2,3,4,5]">
			<image src="@/static/logo.png"></image>
			<view class="title">限时秒杀</view>
		</view>
	</view>
</template>

<script>
</script>

<style lang="scss" scoped>
	// 首页导航部分
	.nav-list {
		background-color: #fff;
		display: flex;
		padding-top: 12rpx;
		.item {
			flex: 1;
			@include flex-center-center;
			flex-direction: column;
			image {
				width: 80rpx;
				height: 80rpx;
			}
			.title {
				padding: 12rpx 0;
				font-size: 28rpx;
			}
		}
	}
</style>