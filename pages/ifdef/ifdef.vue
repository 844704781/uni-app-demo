<template>
	<view class="bbox-5">
		条件编译案例
		<!-- #ifdef H5 -->
		<view>我希望在H5中显示</view>
		<!-- #endif -->
		<!-- #ifdef MP-WEIXIN -->
		<view>我希望在微信中显示</view>
		<!-- #endif -->
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {

		},
		onLoad() {
			// #ifdef H5
			console.log('我希望在H5中打印')
			// #endif
			// #ifdef MP-WEIXIN
			console.log('我希望在微信中打印')
			// #endif
		}
	}
</script>

<style>
	/* #ifdef H5 */
	.bbox-5 {
		color: red
	}
	/* #endif */
	
	/* #ifdef MP-WEIXIN */
	.bbox-5 {
		color: blue
	}
	/* #endif */
</style>
