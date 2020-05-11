<template>
	<view class="container">
		<Item
		v-for='item in menuList'
		:text='item.text'
		:path='item.path'
		></Item>
	</view>
</template>

<script>
	import Item from './menuItem.vue'
	export default{
		props:['menuList'],
		components:{
			Item,
		}
	}
</script>

<style lang="scss">
	.container{
		height:308upx;
		padding-top: 35upx;
		padding-left: 36upx;
		padding-right: 36upx;
		padding-bottom: 50upx;
		box-sizing: border-box;
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
		background:rgba(255,255,255,1);
	}
</style>
