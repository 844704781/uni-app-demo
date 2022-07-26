<template>
	<view>
		这是兄弟组件B1
		<button @click='sendB2'>给兄弟B2传值</button>
	</view>
</template>

<script>

	export default {
		methods:{
			sendB2(){
				uni.$emit('sendB2','wanglaowu')
			}
		}
	}
</script>

<style>
</style>