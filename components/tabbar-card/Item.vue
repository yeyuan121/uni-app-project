<template>
	<view class="containers" @click="handleClick()">
		<image :src="imgpath" mode=""></image>
		<view class="item">
			{{text}}
		</view>
	</view>
</template>

<script>
	export default{
		props:['text','imgpath','id'],
		methods:{
			handleClick(){}
		}
	}
</script>

<style lang="scss" scoped>
	.containers{
		color:rgba(184,186,185,1);
		width: 86upx;
		height: 70upx;
		display: flex;
		flex-direction: column;
		align-items: center;
		image{
			width:50upx;
			height:40upx;
		}
		.item{
			margin-top: 8upx;
			width:86upx;
			height:21upx;
			font-size:22upx;
			font-family:PingFang-SC-Regular;
			font-weight:400;
			// color:rgba(184,186,185,1);
			white-space: nowrap;
			text-align: center;
		}
	}
</style>
