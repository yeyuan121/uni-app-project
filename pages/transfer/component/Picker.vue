<template>
	<view class="container">
		<view class="class1" 
		:class="{add:current == 0}"
		@click='handleClick(0)'
		>
			选择区域
			<view class="direct-container">
				<view class="div1" 
				@click="selectDirect(1)"
				:class="{add1:directionCurrent == 1}"
				></view>
				<view class="div2"></view>	
			</view>
		</view>
		<view class="class2" 
		:class="{add:current == 1}"
		@click='handleClick(1)'
		>
			公司类型
			<view class="direct-container">
				<view class="div1"></view>
				<view class="div2"></view>	
			</view>
		</view>
		<view class="class3" 
		:class="{add:current == 2}"
		@click='handleClick(2)'
		>
			所属行业
			<view class="direct-container">
				<view class="div1"></view>
				<view class="div2"></view>	
			</view>
		</view>
		<view class="class4" 
		:class="{add:current == 3}"
		@click='handleClick(3)'
		>
			更多
			<view class="direct-container">
				<view class="div1"></view>
				<view class="div2"></view>	
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		data(){
			return{
				current:0,
				directionCurrent:1
			}
		},
		methods:{
			handleClick(i){
				this.current = i
			},
			selectDirect(i){
				this.directionCurrent = i
			}
		}
	}
</script>

<style lang="scss">
	.container{
		height:100upx;
		background:rgba(255,255,255,1);
		padding: 37upx 31upx;
		box-sizing: border-box;
		display: flex;
		justify-content: space-between;
		font-size:28upx;
		font-family:PingFang-SC-Regular;
		font-weight:400;
		color:rgba(153,153,153,1);
		.class1,.class2,.class3{
			width: 150upx;
			display: flex;
			align-items: center;
		}
		.class4{
			display: flex;
			align-items: center;
			width: 100upx;
		}
		.div1{
			width: 0;
			height: 0;
			border-right: 8upx solid  transparent;
			border-left: 8upx solid  transparent;
			border-bottom: 8upx solid #A9A9A9;
		}
		.div2{
			width: 0;
			height: 0;
			border-right: 8upx solid  transparent;
			border-left: 8upx solid  transparent;
			border-top: 8upx solid #A9A9A9;
		}
		.direct-container{
			height: 100%;
			padding: 3upx 0;
			padding-top: 5upx;
			box-sizing: border-box;
			margin-left: 9upx;
			display: flex;
			flex-direction: column;
			justify-content: space-between;
		}
		.add{
			font-weight:bold;
			color:rgba(0,0,0,1);
		}
		.add1{
			border-bottom: 8upx solid rgba(255, 89, 89, 1) !important;
		}
	}
</style>
