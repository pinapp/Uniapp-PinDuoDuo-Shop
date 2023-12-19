<style lang="scss">
	page {
		background: #ebedf0;
		min-height: 100vh;
		// 头部
		.header {
			background: #fff;
			padding: 24rpx;
		}
	}
</style>
<template>
	<view>
		<!-- 头部 -->
		<view class="header">
			<home-search></home-search>
		</view>
		
		<!-- 首页导航 -->
		<nav-list></nav-list>
		
		<!-- 百亿补贴 -->
		<home-active></home-active>
		
		<!-- Tap组件 -->
		<home-tab></home-tab>
		
		<!-- 商品组件 -->
		<goods-list></goods-list>
	</view>
</template>

<script>
	import homeSearch from "./component/home-search.vue"
	import navList from "./component/nav-list.vue"
	import homeActive from "./component/home-active.vue"
	import homeTab from "./component/home-tab.vue"
	import goodsList from "./component/goods-list.vue"
	
	export default {
		components: {
			homeSearch,
			navList,
			homeActive,
			homeTab,
			goodsList
		},
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {
		}
	}
</script>