<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
		<view>
			这是父组件
			<test :age='12' @myEvent='setName'></test>
			<view>
				这是子组件传过来的值:{{name}}
			</view>
		</view>

		<view>
			<uni-calendar :insert="true" :lunar="true" :start-date="'2019-3-2'" :end-date="'2019-5-20'"
				@change="change" />
		</view>
	</view>
</template>

<script>
	import test from '@/components/test.vue'

	export default {
		data() {
			return {
				title: 'Hello',
				name: ''
			}
		},
		onLoad() {

		},
		components: {
			'test': test,
		},
		methods: {
			setName(data) {
				this.name = data
			},
			change(e) {
				console.log('触发了change', e)
			}
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
