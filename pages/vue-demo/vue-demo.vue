<template>
	<view>
		<view>
			这是view组件的演示
		</view>
		<view class='bbox1'>
			这是一个普通盒子
		</view>

		<p>-------------------</p>

		<view class='bbox1' hover-class="bbox1-hover">
			这是一个按下去变颜色的盒子
		</view>

		<p>-------------------</p>

		<view class="bbox2" hover-class="bbox2-hover">
			<view class='bbox1' hover-class="bbox1-hover">
				这是一个按下去无法阻止冒泡，两个都会变颜色的盒子
			</view>
		</view>

		<p>-------------------</p>

		<view class="bbox2" hover-class="bbox2-hover">
			<view class='bbox1' hover-class="bbox1-hover" hover-stop-propagation>
				这是一个按下去阻止冒泡，只有一个会变颜色会变颜色的盒子
			</view>
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

<style>
	.bbox1 {
		width: 100px;
		height: 100px;
		background-color: green;
	}

	.bbox2 {
		width: 200px;
		height: 200px;
		background-color: pink;
	}

	.bbox1-hover {
		background-color: blue;
	}

	.bbox2-hover {
		background-color: red;
	}
</style>
