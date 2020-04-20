<template>
	<view>
		<button type="default" @click="toDetail">点击按钮跳转</button>
		<navigator url="../demo/demo">
			<button type="primary">跳转到新页面</button>
		</navigator>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
			}
		},
		onLoad() {

		},
		methods: {
			toDetail(){
				uni.navigateTo({
					url:'../demo/demo'
				})
			}
		}
		
	}
</script>

<style>
</style>
