<template>
	<view>
		<text> 动态绑定class 和 style </text>
		<!--  class 的对象语法, 对象中的key可以不加引号    -->
		<view :class="{ 'active': isActive }">1111</view>
		<!--  class 的数组语法   -->
		<view class="static" :class="[class1, class2]">23333</view>
		<!--  class 的数组语法   -->
		<view class="static" v-bind:class="[isActive ? 'activeClass' : '', 'errorClass']" @tap="isActive = !isActive">34444</view>
		<!--  class 的数组语法   -->
		<view class="static" v-bind:class="[{ 'active': isActive }, 'errorClass']" @tap="isActive = !isActive">45555</view>
		
		
		<view v-bind:style="{ color: activeColor, fontSize: fontSize + 'px' }">666</view>
		<view v-bind:style="[{ color: activeColor, fontSize: fontSize + 'px' }]" style="display: none;">777</view>
		<view v-bind:style="[{ color: activeColor, fontSize: fontSize + 'px' }]">888</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				isActive: true,
				class1: 'activeClass',
				class2: 'errorClass',
				activeColor: '#000000',
				fontSize: 26,
			}
		},
		methods: {
			
		}
	}
</script>

<style>
.active{
	background-color: red;
}
.activeClass{
	background-color: yellow;
}

.errorClass{
	font-size: 32upx;
	font-weight: bold;
	color: #8A6DE9;
}
</style>
