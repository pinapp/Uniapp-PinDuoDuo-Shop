<style lang="scss">
page {
	background: #ebedf0;
	min-height: 100vh;
	.user {
		@include flex-between;
		align-items: center;
		background: #fff;
		padding: 24rpx 32rpx;
		.left {
			@include flex-center;
			image {
				margin-right: 32rpx;
			}
			.option-box {
				.nickname {
					font-size: 42rpx;
					font-weight: bold;
				}
				.button {
					background: palevioletred;
					color: #fff;
					font-size: 24rpx;
					padding: 2rpx 24rpx;
					border-radius: 50rpx;
					margin-top: 8rpx;
				}
			}
		}
		.right {
			border: 1rpx solid darkgray;
			padding: 8rpx 16rpx;
			border-radius: 50rpx;
			font-size: 28rpx;
			image {
				width: 40rpx;
				height: 40rpx;
				margin-right: 8rpx;
			}
			@include flex-center;
		}
		image {
			width: 120rpx;
			height: 120rpx;
			border-radius: 120rpx;
		}
	}
	.order {
		margin-top: 0rpx;
	}
	.order, .fun-nav, .other-nav {
		:deep .header {
			margin-bottom: 42rpx;
		}
		:deep .list {
			@include flex-center;
			.item {
				@include flex-center;
				flex-direction: column;
				flex: 1;
				image {
					width: 100rpx;
					height: 100rpx;
					margin-bottom: 12rpx;
				}
				.title {
					margin-top: 12rpx;
					color: dimgray;
				}
			}
		}
	}
}
</style>

<template>
	<view class="header">
		<!-- 用户信息 -->
		<view class="user">
			<view class="left">
				<image src="@/static/logo.png"></image>
				<view class="option-box">
					<view class="nickname">#</view>
					<view class="button">更新资料</view>
				</view>
			</view>
			<view class="right">
				<image src="@/static/logo.png"></image>
				<view class="button">拼单返现</view>
			</view>
		</view>
		
		<!-- 我的订单 -->
		<card class="order">
			<template #header>
				<view class="header">
					<view class="title">我的订单</view>
					<view class="header-right">
						<view class="right-title">查看全部</view>
						<image src="@/static/logo.png"></image>
					</view>
				</view>
				<view class="content">
					<view class="list">
						<view class="item">
							<image src="@/static/logo.png"></image>	
							<view class="title">待付款</view>
						</view>
						<view class="item">
							<image src="@/static/logo.png"></image>	
							<view class="title">待分享</view>
						</view>
						<view class="item">
							<image src="@/static/logo.png"></image>	
							<view class="title">待发货</view>
						</view>
						<view class="item">
							<image src="@/static/logo.png"></image>	
							<view class="title">待收货</view>
						</view>
						<view class="item">
							<image src="@/static/logo.png"></image>	
							<view class="title">评价</view>
						</view>
					</view>
				</view>
			</template>
		</card>
		
		<!-- 钱包 -->
		<card>
			<template #header>
				<view class="header">
					<view class="title">多多钱包</view>
					<view class="header-right">
						<view class="right-title">查看余额</view>
						<image src="@/static/logo.png"></image>
					</view>
				</view>
				<view class="content">
				</view>
			</template>
		</card>
		
		<!-- 功能导航 -->
		<card class="fun-nav">
			<template #content>
				<view class="content">
					<view class="list">
						<view class="item" v-for="(item, index) in [1,2,3,4,5]">
							<image src="@/static/logo.png"></image>	
							<view class="title">待付款</view>
						</view>
					</view>
				</view>
			</template>
		</card>
		
		<!-- 其他导航 -->
		<card class="other-nav">
			<template #content>
				<view class="content">
					<view class="list">
						<view class="item" v-for="(item, index) in [1,2,3,4,5]">
							<image src="@/static/logo.png"></image>	
							<view class="title">待付款</view>
						</view>
					</view>
				</view>
			</template>
		</card>
	</view>
</template>

<script>
	import card from "./component/card.vue"
	export default {
		components: {
			card
		},
		data() {
			return {}
		},
		methods() {
			
		}
	}
</script>

