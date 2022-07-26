<template>
	<view>
		这是样式案例模块
		<view class='sbox1'>
			rpx最大box
			<p></p>
			<text class="sbox1-text">我是老大吗</text>
		</view>
		<view class="iconfont icon-tupian">
		</view>
	</view>
</template>

<script>
	
	export default {
		data() {
			return {

			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	@import url('./style-demo.css');
	.sbox1 {
		width: 750rpx;
		height: 750rpx;
		background-color: $global-color;;
		text{
			color:blue
		}
	}
</style>
