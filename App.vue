<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		},
		onError:function(e){
			console.log('App Error:',e)
		}
	}
</script>

<style>
	@import url('/static/font/iconfont.css');
	/*每个页面公共css */
	.sbox1-text{
		color: red;
		font-size: 50rpx;
	}
</style>
