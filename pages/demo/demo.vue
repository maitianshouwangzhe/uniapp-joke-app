<template>
	<view class="demo-page">
		<view class="icon iconfont icon-manyidu animated fadeInDownBig"></view>
		<view class="icon iconfont icon-fenlei animated fadeIn"></view>
		<view class="box-1 animated" hover-class="box-1-hover bounce" hover-stay-time="1000">view 标签</view>
		<!--   由于值的类型为Boolen类型， 如果前面不加冒号，则表示是字符串    -->
		<text :selectable="true">这是文本 \n 你好么 </text>
		
		<view class="box-2">
			<text>111</text>
			<view>222</view>
			<view>333</view>
			<view>444</view>
			<text>555</text>
		</view>
		
		
		<view class="box-3" @tap="handleClick1">
			外面
			<view @tap.stop="handleClick2">(在子元素中，需要阻止事件冒泡)里面</view>
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
			handleClick1(){
				console.log('点击外面')
			},
			handleClick2(){
				console.log('点击里面的子元素')
			},
		}
	}
</script>

<style>
.box-1{
	width: 200upx;
	height: 200upx;
	background-color: #007AFF;
	color: #FFFFFF;
	margin: 60upx;
}

.box-1-hover{
	background-color: #8A6DE9;
}


.box-2{
	width: 400upx;
	height: 400upx;
	background-color: #0A98D5;
	padding: 30upx;
}

/* css 3选择器的用法 */
/*  类选择器为box-2的第一个view标签 
 *  或者使用 .box-2>view:first-child
 */
.box-2>view:nth-child(2){
	font-weight: bold;
	color: red;
	font-size: 60upx;
}


.box-2>text:nth-of-type(2){
	font-weight: bold;
	color: yellow;
	font-size: 60upx;
}


.box-3{
	width: 100%;
	height: 400upx;
	background-color: #007AFF;
	display: flex;
	justify-content: center;
	align-items: center;
}
.box-3 view{
	width: 200upx;
	height: 200upx;
	background-color: #FF3333;
	display: flex;
	justify-content: center;
	align-items: center;
}

</style>
