<template>
	<view class="container" :style="{background:backgroundColor}">
		<view class="left">
			<view class="left1">
				{{title}}
			</view>
			<view class="left2">
				{{desc}}
			</view>
		</view>
		<view class="right">
			<image :src="path" mode=""></image>
		</view>
	</view>
</template>

<script>
	export default{
		props:['title','desc','path','backgroundColor'],
		created(){
			console.log(666)
		}
	}
</script>

<style lang="scss">
	.container{
		width:344upx;
		height:150upx;
		background:rgba(242,249,255,1);
		box-shadow:0px 3upx 7upx 0upx rgba(0, 0, 0, 0.1);
		border-radius:10upx;
		margin-bottom: 20upx;
		display:flex;
		.right{
			width:125upx;
			height:137upx;
			border-radius:10upx;
			image{
				height: 100%;
				width: 100%;
			}
		}
		.left{
			flex: 1;
			padding: 31upx 20upx;
			padding-right: 0upx;
			box-sizing: border-box;
			.left1{
				height: 35upx;
				line-height: 35upx;
				font-size:36upx;
				font-family:PingFang-SC-Medium;
				font-weight:bold;
				color:rgba(0,0,0,1);
				margin-bottom: 22upx;
			}
			.left2{
				height:23upx;
				font-size:24upx;
				font-family:PingFang-SC-Regular;
				font-weight:bold;
				color:rgba(147,149,148,1);
				line-height: 23upx;
				white-space: nowrap;
			}
		}
	}
</style>
