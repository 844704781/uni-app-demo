<template>
	<view>
		<button @click='send'>发送请求</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			send(){
				uni.request({
					url:'https://api-hmugo-web.itheima.net/api/public/v1/home/swiperdata',
					success:function(data){
						console.log(data)
					}
				})
			}
		}
	}
</script>

<style>

</style>
