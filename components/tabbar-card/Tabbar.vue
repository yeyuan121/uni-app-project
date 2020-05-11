<template>
	<view class="container">
		<Item
		v-for='item in tabbarList'
		:text='item.name'
		:imgpath='item.path'
		:id='item.id'
		:class='{add:current == item.id}'
		@click.native='handleClick(item.id)'
		>
		</Item>
	</view>
</template>

<script>
	import Item from './Item.vue'
	export default{
		data(){
			return{
				current:0,
				tabbarList:
				[
					{
						path:'/static/img/80.png',
						name:'工商财税',
						id:0,
					},
					{
						path:'/static/img/81.png',
						name:'公司转让',
						id:1,
					},
					{
						path:'/static/img/82.png',
						name:'搞企来',
						id:2,
					},
					{
						path:'/static/img/83.png',
						name:'电商服务',
						id:3,
					},
					{
						path:'/static/img/84.png',
						name:'知识产权',
						id:4,
					}
				]
			}
		},
		created(){
			console.log(this.pageid,222)
			this.current = this.pageid
			this.changeImage(this.current)
		},
		components:{
			Item,
		},
		props:['pageid'],
		methods:{
			handleClick(id){
				this.current = id
				if(id == 0){
					this.tabbarList[id].path = '/static/img/80.png'
					this.tabbarList[1].path = '/static/img/81.png'
					uni.navigateTo({
						url:'/pages/detail/detail?current_id'+this.current
					})
				}else if(id == 1){
					console.log(this.current)
					this.tabbarList[id].path = '/static/img/86.png'
					this.tabbarList[0].path = '/static/img/85.png'
					uni.navigateTo({
						url:'/pages/transfer/transfer?current_id='+this.current
					})
				}
			},
			changeImage(id){
				if(id == 0){
					this.tabbarList[id].path = '/static/img/80.png'
					this.tabbarList[1].path = '/static/img/81.png'
				}else if(id == 1){
					this.tabbarList[id].path = '/static/img/86.png'
					this.tabbarList[0].path = '/static/img/85.png'
				}
			},
		}
	}
</script>

<style lang="scss" scoped>
	.container{
		position: fixed;
		z-index: 1;
		bottom: 0;
		left: 0;
		height:98upx;
		width: 100%;
		background:rgba(255,255,255,1);
		padding: 0 28upx;
		box-sizing: border-box;
		display: flex;
		justify-content: space-between;
		align-items: center;
		.add{
			color:rgba(47,155,253,1) !important;
		}
	}
</style>
