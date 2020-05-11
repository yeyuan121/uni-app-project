<template>
	<view class="container">
		<view class="item"
		:class="{add:current == item.id}"
		v-for="item in selectList"
		@click="handleClick(item.id)"
		>
		{{item.name}}
		<view class="shows" v-if="current == item.id"></view>
		</view>
	</view>
</template>

<script>
	export default{
		props:['selectList',],
		data(){
			return{
				current:0,
			}
		},
		methods:{
			handleClick(id){
				this.current = id
			}
		}
	}
</script>

<style lang="scss">
	.container{
		display: flex;
		align-items: center;
		height:90upx;
		background:rgba(255,255,255,1);
		padding: 29upx 62upx;
		border-bottom: 1upx solid rgba(215,215,215,1);
		box-sizing: border-box;
		view{
			position: relative;
			flex: 1;
			text-align: center;
			font-size:32upx;
			font-family:PingFang-SC-Regular;
			font-weight:400;
			color:rgba(37,37,37,1);
			.shows{
				position: absolute;
				top: 63upx;
				width:50upx;
				height:5upx;
				background:rgba(255,89,89,1);
				border-radius:1upx;
				left: 50%;
				transform: translateX(-50%);
			}
		}
		.add{
			color:rgba(255,89,89,1) !important;
			font-weight: bold !important;
		}
	}
</style>
