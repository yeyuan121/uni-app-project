<template>
	<view class="container">
		<!-- <TimeHeader
		positions='sticky'
		tops='0'
		backgrounds='rgba(255,255,255,1)'
		></TimeHeader> -->
		<Navbar></Navbar>
		<Tabbar 
		pageid='0'>
		</Tabbar>
		<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
			<swiper-item>
				<view class="swiper-item uni-bg-red">
					<image src="../../static/img/10.png" mode="widthFix" style="width: 100%;height: 100%;"></image>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item uni-bg-green">
					<image src="../../static/img/10.png" mode="widthFix" style="width: 100%;height: 100%;"></image>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item uni-bg-blue">
					<image src="../../static/img/10.png" mode="widthFix" style="width: 100%;height: 100%;"></image>
				</view>
			</swiper-item>
		</swiper>
		<menuCard
		:menu-list='menuArrs'
		></menuCard>
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
		<view class="showNav">
			<Item
			v-for='item in dataList'
			:text1='item.text1'
			:text2='item.text2'
			:text3='item.text3'
			:button-bgc='item.buttonBgc'
			:path='item.path'
			></Item>
		</view>
		<selectBar 
		:select-list='arr'
		/>
		<messageItem
		v-for='item in messageArr'
		:path='item.path'
		:text1='item.msg1'
		:text2='item.msg2'
		>		
		</messageItem>
	</view>
</template>

<script>
	import TimeHeader from '../../components/timeHeader-card/TimeCard.vue'
	import Tabbar from '../../components/tabbar-card/Tabbar.vue'
	import Item from './component/item.vue'
	import selectBar from '../../components/select-card/selectCard.vue'
	import menuCard from '../../components/menu-card/menuCard.vue'
	import messageItem from './component/Message.vue'
	import Navbar from '../../components/navbar-card/Navbar.vue'
	export default{
		data(){
			return{
				background: ['color1', 'color2', 'color3'],
				indicatorDots: false,
				autoplay: true,
				interval: 2000,
				duration: 500,
				dataList:[
					{
						text1:'注册公司',
						text2:'秒杀',
						text3:'快速发照',
						buttonBgc:'rgba(210,160,64,1)',
						path:'/static/img/30.png'
					},
					{
						text1:'团购',
						text2:'记账产品',
						text3:'限时低价',
						buttonBgc:'rgba(229,133,91,1)',
						path:'/static/img/31.png'
					},
					{
						text1:'我要成为',
						text2:'工商跑腿专员',
						text3:'立即成为',
						buttonBgc:'rgba(89,132,237,1)',
						path:'/static/img/32.png'
					},
					{
						text1:'我要成为',
						text2:'会计师',
						text3:'限时低价',
						buttonBgc:'rgba(229,133,91,1)',
						path:'/static/img/33.png'
					},
				],
				arr:
				[
					{
						name:"工商变更",
						id:0,
					},
					{
						name:'会计记账',
						id:1,
					},
					{
						name:'资质服务',
						id:2,
					}
				],
				menuArrs:
				[
					{
						text:'注册变更',
						id:0,
						path:'/static/img/40.png'
					},
					{
						text:'财税代办',
						id:0,
						path:'/static/img/41.png'
					},
					{
						text:'刻章',
						id:0,
						path:'/static/img/42.png'
					},
					{
						text:'资质代办',
						id:0,
						path:'/static/img/43.png'
					},
					{
						text:'公司注销',
						id:0,
						path:'/static/img/44.png'
					},
					{
						text:'落户咨询',
						id:0,
						path:'/static/img/45.png'
					},
					{
						text:'贷款咨询',
						id:0,
						path:'/static/img/46.png'
					},
					{
						text:'更多服务',
						id:0,
						path:'/static/img/47.png'
					},
				],
				messageArr:
				[
					{
						path:'/static/img/9.png',
						msg1:'个体工商户注册',
						msg2:'副标题副标题副标题副标题副标题副标题'
					},
					{
						path:'/static/img/9.png',
						msg1:'个体工商户注册',
						msg2:'副标题副标题副标题副标题副标题副标题'
					},
					{
						path:'/static/img/9.png',
						msg1:'个体工商户注册',
						msg2:'副标题副标题副标题副标题副标题副标题'
					},
				]
			}
		},
		components:{
			Item,
			selectBar,
			menuCard,
			messageItem,
			Navbar,
			Tabbar,
			TimeHeader,
		}
	}
</script>

<style lang="scss">
	.container{
		.swiper{
			height: 291upx;
		}
		.menu{
			height:308upx;
			background:rgba(255,255,255,1);
			padding: 35upx 36upx;
			box-sizing: border-box;
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
				font-family:PingFang SC;
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
		.showNav{
			height: 363upx;
			background:rgba(242,242,242,1);
			padding: 20upx 30upx;
			box-sizing: border-box;
			display: flex;
			flex-wrap: wrap;
			justify-content: space-between;
			align-content: flex-start;
		}
	}
</style>
