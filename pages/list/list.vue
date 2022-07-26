<template>
	<view class='bbox-3'>
		下拉刷新案例
		<view class='bbox-4' v-for="item in list">{{item}}</view>
		<button @click="onPull">下拉刷新按钮</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: ['JAVA', 'Android', 'PHP', 'Python', 'Golang','JAVA', 'Android', 'PHP', 'Python', 'Golang']
			}
		},
		onPullDownRefresh: function() {
			console.log('触发下拉刷新')
			this.list = ['Android', 'PHP', 'JAVA', 'Python', 'Golang']
		},
		onReachBottom: function() {
			console.log('页面触底刷新')
			this.list = [...this.list, ...this.list]
		},
		methods: {
			onPull() {
				console.log('点击触发下拉刷新')
				uni.startPullDownRefresh()
			}
		}
	}
</script>

<style>
	.bbox-3 {
/* 		border: solid 1px red; */
/* 		height: 500px; */
	}
	.bbox-4{
		margin-bottom:50px;
	}
</style>
