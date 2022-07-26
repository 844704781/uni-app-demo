<template>
	<view>
		<button @click="setData">异步设置数据</button>
		<button @click="setDataSync">同步设置数据</button>
		<button @click='getData'>异步获取数据</button>
		<button @click='getDataSync'>同步获取数据</button>
		<button @click='removeData'>异步删除数据</button>
		<button @click='removeDataSync'>同步删除数据</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {
			setData() {
				uni.setStorage({
					key: 'username',
					data: '张三',
					success() {
						console.log('异步设置成功')
					}
				})
			},
			setDataSync() {
				uni.setStorageSync('username', '张三')
				console.log('同步设置成功')
			},
			getData() {
				uni.getStorage({
					key: 'username',
					success(data) {
						console.log('异步获取成功', data)
					}
				})
			},
			getDataSync() {
				const data = uni.getStorageSync('username')
				console.log('同步获取成功', data)
			},
			removeData() {
				uni.removeStorage({
					key: 'username',
					success() {
						console.log('异步删除成功')
					}
				})
			},
			removeDataSync() {
				uni.removeStorageSync('username')
				console.log('同步删除成功')
			}
		}
	}
</script>

<style>

</style>
