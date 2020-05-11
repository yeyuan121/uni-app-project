<template>
	<view class="container">
		<!-- <TimeHead
		positions='sticky'
		tops='0'
		backgrounds='rgba(255,255,255,1)'
		></TimeHead> -->
		<Tabbar
		pageid='1'
		></Tabbar>
		<Nav></Nav>
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
		<Menu
		:menuList='menuArr'
		/>
		<view class="title">
			<view class="title1">
				资讯
			</view>
			<view class="title2">
				头条
			</view>
			<view class="title3">
				最新成交：***公司成交4000万
			</view>
			<!-- <view class="title4">
				NEW
			</view> -->
			<view class="title5">
				更多>
			</view>
		</view>
		<view class="item-flex-container">
			<Item
			v-for='item in itemArr'
			:text1='item.text1'
			:text2='item.text2'
			:text3='item.text3'
			:button-bgc='item.buttonbgc'
			:background='item.background'
			:path='item.path'
			/>
			<image src="../../static/img/11.png" mode="widthFix"></image>
		</view>
		<SelectTab
		:select-list='selectArr'
		/>
		<Pickers/>
		<view class="whitespace"></view>
		<MessageItem
		v-for='item in 3'
		message1='【转让中】厦门***投资管理公司'
		message2='2000'
		message3='小规模'
		message4='2015-05-12'
		message5='2018-06-05'
		message6='2000.00'
		message7='2000.00'
		/>
	</view>
</template>

<script>
	import MessageItem from './component/Message.vue'
	import Pickers from './component/Picker.vue'
	
	import TimeHead from '../../components/timeHeader-card/TimeCard.vue'
	import Tabbar from '../../components/tabbar-card/Tabbar.vue'
	import Nav from '../../components/navbar-card/Navbar.vue'
	import Menu from '../../components/menu-card/menuCard.vue'
	import Item from '../detail/component/item.vue'
	import SelectTab from '../../components/select-card/selectCard.vue'
	export default{
		onLoad(option){
			console.log(option.current_id)
		},
		data(){
			return{
				background: ['color1', 'color2', 'color3'],
				indicatorDots: false,
				autoplay: true,
				interval: 2000,
				duration: 500,
				menuArr:
				[
					{
						path:'/static/img/20.png',
						text:'贸易电商'
					},
					{
						path:'/static/img/21.png',
						text:'服饰鞋包'
					},{
						path:'/static/img/22.png',
						text:'广告传媒'
					},{
						path:'/static/img/23.png',
						text:'服务咨询'
					},{
						path:'/static/img/24.png',
						text:'工程建设'
					},
					{
						path:'/static/img/25.png',
						text:'金融保险'
					},{
						path:'/static/img/26.png',
						text:'人力劳务'
					},{
						path:'/static/img/27.png',
						text:'科技研发'
					},
				],
				itemArr:
				[
					{
						text1:'公司转让',
						text2:'价值评估',
						text3:'快速发布',
						buttonbgc:'rgba(210,160,64,1)',
						background:'rgba(255,252,244,1)',
						path:'/static/img/28.png'
					},
					{
						text1:'我要求购公司',
						text2:'欢迎选购',
						text3:'快速查找',
						buttonbgc:'rgba(229,133,91,1)',
						background:'rgba(255,242,230,1)',
						path:'/static/img/29.png'
					},
				],
				selectArr:
				[
					{
						name:'今日看点',
						id:0
					},
					{
						name:'精品推荐',
						id:1
					},
					{
						name:'特价推荐',
						id:2
					},
				]
			}
		},
		components:{
			Menu,
			Item,
			SelectTab,
			MessageItem,
			Pickers,
			Nav,
			Tabbar,
			TimeHead,
		}
	}
</script>

<style lang="scss">
	.container{
		.swiper{
			height: 291upx;
		}
		.whitespace{
			height: 20upx;
			background:rgba(242,242,242,1);
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
				width:388upx;
				height:26upx;
				font-size:28upx;
				font-family:PingFang-SC-Regular;
				font-weight:400;
				color:rgba(107,108,112,1);
				white-space: nowrap;
				// overflow: hidden;
				line-height: 26upx;
				letter-spacing: -2upx;
				margin-right: 81upx;
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
		.item-flex-container{
			display: flex;
			flex-wrap: wrap;
			justify-content: space-between;
			padding: 20upx 30upx;
			box-sizing: border-box;
			background:rgba(242,242,242,1);
			image{
				width:100%;
				height:150upx;
				border-radius:4upx;
			}
		}
	}
</style>
