<template>
	<view class="container">
		<image :src="path" mode=""></image>
		<view class="message">
			<view class="view1">
				{{text1}}
			</view>
			<view class="view2">
				{{text2}}
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		props:['path','text1','text2']
	}
</script>

<style lang="scss">
	.container{
		display: flex;
		height:176upx;
		padding-top: 32upx;
		padding-left: 28upx;
		padding-bottom: 27upx;
		box-sizing: border-box;
		background:rgba(255,255,255,1);
		border:1upx solid rgba(243,243,245,1);
		image{
			width:119upx;
			height:117upx;
			border-radius:4upx;
			margin-right: 16upx;
		}
		.message{
			flex:1;
			.view1{
				height:31upx;
				line-height: 31upx;
				font-size:32upx;
				font-family:PingFang-SC-Medium;
				font-weight:500;
				color:rgba(51,51,51,1);
				margin-bottom: 24upx;
			}
			.view2{
				font-size:24upx;
				font-family:PingFang-SC-Regular;
				font-weight:400;
				color:rgba(162,162,162,1);
			}
		}
	}
</style>
