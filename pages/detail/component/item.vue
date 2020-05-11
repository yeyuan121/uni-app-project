<template>
	<view class="container" :style="{background:background}">
		<view class="left">
			<view class="left1">
				{{text1}}
			</view>
			<view class="left2">
				{{text2}}
			</view>
			<view class="left3" :style="{background:buttonBgc}">
				{{text3}}>
			</view>
		</view>
		<view class="right">
			<image :src="path" mode=""></image>
		</view>
	</view>
</template>

<script>
	export default{
		props:['text1','text2','text3','buttonBgc','background','path']
	}
</script>

<style lang="scss">
	.container{
		width:328upx;
		height:150upx;
		// padding: 24upx 17upx;
		box-sizing: border-box;
		background:rgba(255,255,255,1);
		border-radius:4upx;
		display: flex;
		margin-bottom: 20upx;
		.left{
			width: 205upx;
			height: 100%;
			padding: 24upx 17upx;
			box-sizing: border-box;
			.left1{
				height:31upx;
				line-height: 31upx;
				font-size:32upx;
				font-family:PingFang-SC-Heavy;
				font-weight:bold;
				color:rgba(51,51,51,1);
				white-space: nowrap;
			}
			.left2{
				height:18upx;
				font-size:20upx;
				font-family:PingFang SC;
				font-weight:400;
				color:rgba(167,169,167,1);
				margin-bottom: 24upx;
				margin-top: 8upx;
			}
			.left3{
				width:108upx;
				height:30upx;
				box-shadow:0upx 3upx 7upx 0upx rgba(229, 88, 134, 0.35);
				border-radius:15upx;
				font-size:18upx;
				font-family:PingFang-SC-Regular;
				font-weight:400;
				color:rgba(255,255,255,1);
				text-align: center;
				line-height: 30upx;
			}
		}
		.right{
			flex: 1;
			image{
				height: 100%;
				width: 100%;
			}
		}
	}
</style>
