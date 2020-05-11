<template>
	<view class="container">
		<!-- <TimeHeader
		positions='fixed'
		tops='0upx'
		></TimeHeader> -->
		<Nav />
		<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
			<swiper-item>
				<view class="swiper-item uni-bg-red">
					<image src="../../static/img/10.png" mode="" style="width: 100%;height: 100%;"></image>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item uni-bg-green">
					<image src="../../static/img/10.png" mode="" style="width: 100%;height: 100%;"></image>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item uni-bg-blue">
					<image src="../../static/img/10.png" mode="" style="width: 100%;height: 100%;"></image>
				</view>
			</swiper-item>
		</swiper>
		<view class="title">
			<view class="title1">
				资讯
			</view>
			<view class="title2">
				头条
			</view>
			<view class="title3">
				2020搞企来服务销售冠军
			</view>
			<view class="title4">
				NEW
			</view>
			<view class="title5">
				更多>
			</view>
		</view>
		<view class="grid-container">
			<Item
			v-for='v in itemArr'
			:title='v.title'
			:desc='v.desc'
			:path='v.path'
			:background-color='v.bgc'
			@click.native='handleClick(v)'
			>
			</Item>
		</view>
	</view>
</template>

<script>
	import Item from './component/item.vue'
	import Nav from './component/Navbar.vue'
	
	import TimeHeader from '../../components/timeHeader-card/TimeCard.vue'
	export default {
		data() {
			return {
				background: ['color1', 'color2', 'color3'],
				indicatorDots: false,
				autoplay: true,
				interval: 2000,
				duration: 500,
				itemArr:[
					{
						title:'工商财税',
						desc:'注册公司 代理记账',
						path:'/static/img/60.png',
						bgc:'white'
					},
					{
						title:'公司转让',
						desc:'公司急售 精品推荐',
						path:'/static/img/61.png',
						bgc:'rgba(255,246,246,1)'
					},
					{
						title:'知识产权',
						desc:'商标注册 商标查询',
						path:'/static/img/62.png',
						bgc:'rgba(250,250,250,1)'
					},
					{
						title:'电商服务',
						desc:'网店代入驻 天猫转让',
						path:'/static/img/63.png',
						bgc:'rgba(248,253,255,1)'
					},
					{
						title:'应用商城',
						desc:'商城系统 直播商城',
						path:'/static/img/64.png',
						bgc:'rgba(253,247,255,1)'
					},
					{
						title:'会员中心',
						desc:'会员服务 订单查询',
						path:'/static/img/65.png',
						bgc:'rgba(255,251,238,1)'
					},
					{
						title:'加盟我们',
						desc:'加入成为合伙人',
						path:'/static/img/66.png',
						bgc:'rgba(255,251,244,1)'
					},
					{
						title:'关于我们',
						desc:'搞企来文化介绍',
						path:'/static/img/67.png',
						bgc:'rgba(241,241,241,1)'
					},
				]
			}
		},
		methods: {
			handleClick(e){
				if(e.title == '工商财税'){
					uni.navigateTo({
						url:'../detail/detail'
					})
				}else if(e.title == '公司转让'){
					uni.navigateTo({
						url:'/pages/transfer/transfer'
					})
				}
			}
		},
		components:{
			Item,
			Nav,
			TimeHeader,
		}
	}
</script>

<style lang="scss">
	// @font-face {
	// 	font-family: PingFang SC;
	// 	src: url('/static/PingFang-SC-Regular.ttf');
	// }
	view{
		letter-spacing: 3upx;
		font-family: PingFang SC;
	}
	.container {
		// padding: 20px;
		font-size: 14px;
		line-height: 24px;
		.swiper{
			height: 423upx;
		}
		.swiper-item{
			height: 100%;
			background-color: green;
		}
		.title{
			display: flex;
			align-items: center;
			height:92upx;
			background:rgba(255,255,255,1);
			padding: 29upx 27upx;
			box-sizing: border-box;
			.title1{
				height: 34upx;
				width: 72upx;
				font-size:36upx;
				font-family:FZCuHeiSongS-B-GB;
				font-weight:400;
				color:rgba(117,117,117,1);
				// line-height:88upx;
				white-space: nowrap;
				line-height: 34upx;
			}
			.title2{
				width:70upx;
				height:35upx;
				background:rgba(251,135,0,1);
				border-radius:6upx;
				font-size:28upx;
				font-family:PingFang-SC-Regular;
				font-weight:500;
				color:rgba(255,255,255,1);
				line-height: 35upx;
				text-align: center;
				margin-right: 21upx;
				margin-left: 6upx;
			}
			.title3{
				width:317upx;
				height:26upx;
				font-size:28upx;
				font-family:PingFang-SC-Regular;
				font-weight:400;
				color:rgba(107,108,112,1);
				white-space: nowrap;
				// overflow: hidden;
				line-height: 26upx;
				letter-spacing: -2upx;
			}
			.title4{
				width:70upx;
				height:35upx;
				background:rgba(255,89,89,1);
				border-radius:18upx;
				font-size:20upx;
				font-family:PingFang-SC-Medium;
				font-weight:500;
				color:rgba(255,255,255,1);
				line-height: 35upx;
				text-align: center;
				margin-right: 71upx;
				margin-left: 11upx;
			}
			.title5{
				width:66upx;
				height:23upx;
				font-size:24upx;
				font-family:PingFang-SC-Regular;
				font-weight:400;
				color:rgba(102,102,102,1);
				line-height: 23upx;
				white-space: nowrap;
			}
		}
		.grid-container{
			height:819upx;
			background:rgba(242,242,242,1);
			padding: 20upx;
			box-sizing: border-box;
			display: flex;
			justify-content: space-between;
			align-content: flex-start;
			flex-wrap: wrap;
		}
	}
</style>
