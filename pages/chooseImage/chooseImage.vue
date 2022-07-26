<template>
	<view>
		<view>图片选择，图片预览案例</view>
		<button @click='chooseImage'>选择图片</button>
		<image v-for="item in images" :src='item' @click='preImage(item)'></image>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				images: []
			}
		},
		methods: {
			chooseImage(e) {
				uni.chooseImage({
					count: 5,
					sourceType: ['album', 'camera'],
					success: (data) => {
						this.images = data.tempFilePaths
						console.log(this.images)
					}
				})
			},
			preImage(item) {
				uni.previewImage({
					current: item,
					urls: this.images
				})
			}
		}
	}
</script>

<style>

</style>
