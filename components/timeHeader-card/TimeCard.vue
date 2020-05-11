<template>
	<view 
	class="container" 
	:style="{
		position:positions,
		top:tops,
		background:backgrounds
	}">
		<image src="../../static/img/77.png" mode="widthFix"></image>
	</view>
</template>

<script>
	export default{
		props:['positions','tops','backgrounds']
	}
</script>

<style lang="scss">
	.container{
		// position: sticky;
		display: flex;
		// align-items: center;
		z-index: 3;
		// top: 0upx;
		width: 100%;
		height:44upx;
		// background:rgba(255,255,255,1);
		image{
			height: 100%;
			width: 100%;
		}
	}
</style>
