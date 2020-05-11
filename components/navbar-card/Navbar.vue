<template>
	<view class="container">
		<view class="view1" @click="back()">
			<image src="../../static/img/70.png" mode=""></image>
		</view>
		<view class="view2">
			<view class="view2child1">
				厦门
				<image src="../../static/img/72.png" mode=""></image>
			</view>
			<view class="view2child2">
				<input 
				type="text" 
				value="" 
				placeholder="搜索服务"
				placeholder-class='placeholderclass'
				/>
			</view>
		</view>
		<view class="view3">
			<image src="../../static/img/71.png" mode=""></image>
		</view>
	</view>
</template>

<script>
	export default{
		methods:{
			back(){
				uni.navigateBack({
					
				})
			}
		}
	}
</script>

<style lang="scss">
	.container{
		height:88upx;
		background:rgba(255,255,255,1);
		padding-left: 41upx;
		padding-right: 30upx;
		box-sizing: border-box;
		display: flex;
		align-items: center;
		/* #ifdef MP-WEIXIN */
		margin-top: 44rpx;
		/* #endif */
		.view1{
			width:40upx;
			height:40upx;
			image{
				height: 100%;
				width: 100%;
			}
		}
		.view2{
			flex:1;
			display: flex;
			align-items: center;
			justify-content: center;
			height: 100%;
			.view2child1{
				display: flex;
				align-items: center;
				justify-content: center;
				width:140upx;
				height:60upx;
				line-height: 60upx;
				text-align: center;
				border:2upx solid rgba(232,232,232,1);
				padding-left: 31upx;
				box-sizing: border-box;
				border-radius:30upx 0px 0px 30upx;
				font-size:28upx;
				font-family:PingFang-SC-Regular;
				font-weight:400;
				color:rgba(102,102,102,1);
				image{
					height: 40upx;
					width: 50upx;
					transform: translateY(5upx);
				}
			}
			.view2child2{
				width:354upx;
				height:60upx;
				line-height: 60upx;
				background:rgba(232,232,232,1);
				border-radius:0px 30upx 30upx 0px;
				font-size:28upx;
				font-family:PingFang-SC-Regular;
				font-weight:400;
				color:rgba(153,153,153,1);
				padding-left: 31upx;
				box-sizing: border-box;
				display: flex;
				align-items: center;
			}
		}
		.view3{
			width:36upx;
			height:29upx;
			position: relative;
			image{
				position: absolute;
				top: 0;
				left: 0;
				height: 100%;
				width: 100%;
			}
		}
		.placeholderclass{
			font-size:28upx;
			font-family:PingFang SC;
			font-weight:400;
			color:rgba(153,153,153,1);
		}
	}
</style>
