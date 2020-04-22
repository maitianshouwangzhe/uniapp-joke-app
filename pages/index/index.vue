<template>
	<view class="index-page">
		
		<view class="index-list" v-for="(item, index) in 16">
			<view class="avartar_add">
				<view class="avartar_user">
					<image src="../../static/bgImg/2.jpg" lazy-load mode="heightFix"></image>
					<text>麦穗</text>
				</view>
				<view class="guanzhu_delete">
					<view class="guanzhu">
						<view class="icon iconfont icon-zengjia"></view>
						<text>关注</text>
					</view>
					<view class="icon iconfont icon-guanbi"></view>
				</view>
			</view>
			<view class="title">好美丽的风景画好美丽的风景画好</view>
			<view class="photo_video">
				<image src="../../static/bgImg/11.jpg"></image>
				<view class="icon iconfont icon-bofang video"></view>
				<view class="video_play_info">20w次播放  2:46</view>
			</view>
			<view class="like_share">
				<view class="islike">
					<view class="icon iconfont icon-icon_xiaolian-mian"></view>
					<text>99</text>
					<view class="icon iconfont icon-kulian"></view>
					<text>0</text>
				</view>
				<view class="share">
					<view class="icon iconfont icon-pinglun1"></view>
					<text>66</text>
					<view class="icon iconfont icon-zhuanfa"></view>
					<text>19</text>
				</view>
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
		onLoad() {

		},
		methods: {
			
		}
		
	}
</script>

<style>
	.index-list{
		padding: 20upx 20upx 25upx 20upx;
		border-bottom: 2upx solid #EFEFEF;
		display: flex;
		flex-direction: column;
	}
	.avartar_add{
		display: flex;
		justify-content: space-between;
		align-items: center;
	}
	.avartar_user *{
		display: inline-block;
		vertical-align: middle;
	}
	.avartar_add image{
		width: 60upx;
		height: 60upx;
		margin-right: 10upx;
		border-radius: 100%;
	}
	.avartar_add .avartar_user text{
		font-size: 30upx;
		color: #989898;
	}
	.guanzhu_delete *{
		display: inline-block;
		vertical-align: middle;
	}
	.guanzhu_delete>view:last-of-type{
		margin-left: 16upx;
		color: #989898;
	}
	.guanzhu {
		background-color: #F4F4F4;
		padding: 6upx 10upx;
	}
	.guanzhu view {
		margin-right: 5upx;
	}
	
	.title{
		font-size: 35upx;
		margin-top: 15upx;
	}
	.photo_video{
		position: relative;
		height: 400upx;
		line-height: 1!important;
	}
	.photo_video image{
		width: 100%;
		border-radius: 3%;
		height: 100%;
	}
	
	.photo_video .video {
		position: absolute;
		font-size: 100upx;
		color: #FFFFFF;
		top: 50%;
		left: 50%;
		margin-left: -50upx;
		/* 由于view组件的行高为1.8, 则需要将其字体的一半乘以1.8   */
		margin-top: -90upx;
	}
	
	.photo_video .video_play_info {
		position: absolute;
		bottom: 20upx;
		right: 15upx;
		background-color: #50573A;
		opacity: 0.7;
		border-radius: 40upx;
		padding: 8upx 25upx;
		font-size: 25upx;
		color: #FFFFFF;
	}
	
	.like_share{
		display: flex;
		justify-content: space-between;
		align-items: center;
	}
	.like_share *{
		display: inline-block;
		color: #D5D5D5;
	}
	
	.like_share>view>view:last-of-type{
		margin: 0 15upx;
	}
	.like_share>view>view:first-of-type{
		margin-right: 15upx;
	}
</style>
