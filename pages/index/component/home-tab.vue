<style lang="scss">
	.list {
		background: #fff;
		margin-top: 24rpx;
		:deep .uni-scroll-view-content {
			display: flex;
		}
		:deep ::-webkit-scrollbar {
			display: none;
			width: 0;
			height: 0;
		}
		.item {
			padding: 24rpx 32rpx;
			flex: none;
			position: relative;
		}
		.item-active {
			color: red;
		}
		.item-active::after {
			content: "";
			display: block;
			left: 0;
			bottom: 0;
			right: 0;
			height: 4rpx;
			background-color: red;
			border-radius: 4rpx;
			margin-top: 12rpx;
		}
	}
</style>

<template>
	<scroll-view  scroll-with-animation="true" scroll-x="" class="list" :scroll-left="scrollLeft">
		<view @click="tabTopChange($event, item, index)" class="item" v-for="(item, index) in [1,2,3,4,5,6,7,8,9,10,11,12]" :class="{'item-active': value == item}">热门</view>
	</scroll-view>
</template>

<script>
	export default {
		data() {
			return {
				value: 1,
				scrollLeft: 0,
				scrollViewWidth: 0
			}
		},
		mounted() {
			uni.createSelectorQuery().select('.list').boundingClientRect((rect)=>{
			 this.scrollViewWidth = Math.round(rect.width)
			}).exec()
		},
		methods: {
			tabTopChange(e, item, index) {
				this.value = item
				let offsetLeft = e.currentTarget.offsetLeft
				this.scrollLeft = offsetLeft - this.scrollViewWidth / 2
			}
		}
	}
</script>