<template>
	<view class="container">
		<view class="view1">
			切换城市>
		</view>
		<view class="view2">
			搞企来
		</view>
		<view class="view3">
			<view class="">
				
			</view>
			<view class="">
				
			</view>
			<view class="">
				
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		
	}
</script>

<style lang="scss">
	.container{
		padding: 0 28upx;
		height: 34upx;
		width: 100%;
		box-sizing: border-box;
		display: flex;
		align-items: center;
		position: absolute;
		top:72upx;
		left:0;
		z-index: 1;
		.view1{
			width: 150upx;
			height:23upx;
			line-height: 23upx;
			font-size:24upx;
			font-family:PingFang-SC-Regular;
			font-weight:500;
			color:rgba(255,255,255,1);
			letter-spacing: normal;
		}
		.view2{
			flex: 1;
			line-height: 34upx;
			font-size:36upx;
			font-family:PingFang-SC-Regular;
			font-weight:bold;
			color:rgba(255,255,255,1);
			white-space: nowrap;
			text-indent: 145upx;
		}
		.view3{
			height: 36upx;
			width: 36upx;
			padding: 2upx 0upx;
			box-sizing: border-box;
			display: flex;
			flex-direction: column;
			justify-content: space-between;
			view{
				height: 5upx;
				background: white;
				border-radius: 1upx;
			}
		}
	}
</style>
