<template>
	<view class="containers">
		<image :src="path" mode=""></image>
		<view class="text">
			{{text}}
		</view>
	</view>
</template>

<script>
	export default{
		props:['text','path']
	}
</script>

<style lang="scss">
	.containers{
		width:140upx;
		height:102upx;
		font-size:28upx;
		font-family:PingFang SC;
		font-weight:400;
		color:rgba(108,108,108,1);
		display: flex;
		flex-direction: column;
		align-items: center;
		margin-bottom: 20upx;
		image{
			width:40upx;
			height:42upx;
			margin-bottom: 25upx;
			box-shadow:0upx 3upx 7upx 0upx rgba(77, 136, 187, 0.35);
		}
		.text{
			font-size:28upx;
			font-family:PingFang-SC-Regular;
			font-weight:400;
			color:rgba(108,108,108,1);
		}
	}
</style>
