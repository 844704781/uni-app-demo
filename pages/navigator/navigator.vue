<template>
	<view>
		路由跳转案例
		<navigator url="/pages/detail/detail">带后退按钮的跳转，不销毁当前页</navigator>
		<navigator url="/pages/message/index" open-type="switchTab">跳转到信息页</navigator>
		<navigator url="/pages/detail/detail" open-type="redirect">重定向跳转，销毁当前页</navigator>
		<button @click="goDetail">带后退按钮的跳转，不销毁当前页</button>
		<button @click="goMessage">跳转到信息页</button>
		<button @click="redirectDetail">重定向跳转，销毁当前页</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {
			goDetail() {
				uni.navigateTo({
					url: '/pages/detail/detail'
				})
			},
			goMessage() {
				uni.switchTab({
					url: '/pages/message/index'
				})
			},
			redirectDetail() {
				uni.redirectTo({
					url: '/pages/detail/detail'
				})
			}
		}
	}
</script>

<style>

</style>
