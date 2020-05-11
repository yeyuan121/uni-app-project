<template>
	<view class="container">
		<view class="class1">
			<text class="class1span1">{{message1}}</text>
			<text class="class1span2">特价</text>
		</view>
		<view class="class2">
			<view class="class2div1">注册资本：{{message2}}万元</view>
			<view class="class2div2">纳税类型：{{message3}}</view>
		</view>
		<view class="class3">
			<view class="class3div1">成立：{{message4}}</view>
			<view class="class3div2">时间：{{message5}}</view>
		</view>
		<view class="class4">
			<view class="class4div1">￥{{message6}}</view>
			<view class="class4div2">￥{{message7}}</view>
		</view>
		<view class="absolute">
			
		</view>
	</view>
</template>

<script>
	export default{
		props:['message1','message2','message3','message4','message5','message6','message7']
	}
</script>

<style lang="scss">
	.container{
		height:206upx;
		background:rgba(255,255,255,1);
		padding: 29upx 32upx;
		box-sizing: border-box;
		position: relative;
		.class1{
			height: 35upx;
			font-size:36upx;
			font-family:PingFang-SC-Regular;
			font-weight:bold;
			color:rgba(51,51,51,1);
			line-height:35upx;
			display: flex;
			justify-content: space-between;
			align-items: center;
			.class1span2{
				width:60upx;
				height:30upx;
				line-height: 30upx;
				background:rgba(241,68,51,1);
				border:1upx solid rgba(241,68,51,1);
				border-radius:4upx;
				font-size:18upx;
				font-family:PingFang-SC-Regular;
				font-weight:400;
				color:rgba(255,255,255,1);
				display: inline-block;
				text-align: center;
			}
		}
		.class2{
			font-size:24upx;
			font-family:PingFang-SC-Regular;
			font-weight:400;
			color:rgba(51,51,51,1);
			line-height:23upx;
			height: 23upx;
			margin-top: 16upx;
			margin-bottom: 19upx;
			display: flex;
			justify-content: space-between;
		}
		.class3{
			height: 22upx;
			margin-bottom: 19upx;
			font-size:24upx;
			font-family:PingFang-SC-Regular;
			font-weight:400;
			color:rgba(51,51,51,1);
			line-height:22upx;
			display: flex;
			justify-content: space-between;
		}
		.class4{
			height: 24upx;
			display: flex;
			.class4div1{
				font-size:30upx;
				font-family:PingFang-SC-Heavy;
				font-weight:bold;
				color:rgba(255,89,89,1);
				line-height:24upx;
				margin-right: 19upx;
			}
			.class4div2{
				font-size:24upx;
				font-family:PingFang-SC-Regular;
				font-weight:400;
				text-decoration:line-through;
				color:rgba(51,51,51,1);
				line-height:24upx;
			}
		}
		.absolute{
			position: absolute;
			bottom: 0;
			right: 0;
			width:625upx;
			height:1upx;
			background:rgba(242,242,242,1);
		}
	}
</style>
