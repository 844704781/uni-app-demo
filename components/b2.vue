<template>
	<view>
		这是兄弟组件B2
		B1发过来的值为:{{name}}
	</view>
</template>

<script>

	export default {
		data(){
			return {
				name : null,
			}
		},
		beforeCreate() {
			uni.$on('sendB2',(data)=>{
				this.name = data
			})
		}
	}
</script>

<style>
</style>