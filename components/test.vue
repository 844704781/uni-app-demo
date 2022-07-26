<template>
	<view>
		这是子组件
		<view>
			-----父组件传过来的age:{{age}}-----
		</view>
		<view>
			<button @click='setParentValue'>给父组件传值</button>
		</view>
		<b1></b1>
		<b2></b2>
	</view>
</template>

<script>
	import b1 from '@/components/b1.vue'
	import b2 from '@/components/b2.vue'

	export default {
		props: ['age'],
		components: {
			'b1': b1,
			'b2': b2
		},
		methods:{
			setParentValue(){
				this.$emit('myEvent','zhangsan')
			}
		}
	}
</script>

<style>
</style>
