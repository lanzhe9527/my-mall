<template>
	<view>
		<!-- 轮播图 -->
		<swiper-images :resdata="swipers"></swiper-images>
		<!-- 首页分类 -->
		<nav-icon :iconNav="iconArray"></nav-icon>
		<!-- 全局分割线 -->
		<divider></divider>
		
		<three-adv :advdata="threeeAdv"></three-adv>
		
		<!-- 全局分割线 -->
		<divider></divider>
		
		<view class="card-box">
			<!-- 标题 -->
			<view class="" style="font-size: 30rpx;font-weight:500;
							border-bottom: 1rpx solid #f1f1f1;;padding: 10rpx 20rpx">每日推荐</view>
		<image src="../../static/images/demo/demo8.jpg" mode="widthFix"></image>
		</view>
		
		
	</view>
</template>

<script>
	import swiperImages from "@/components/index/swiper-images.vue"
	import navIcon from "@/components/index/index-nav.vue"
	import threeAdv from "@/components/index/three-adv.vue"
	export default {
		components:{
			swiperImages,
			navIcon,
			threeAdv
		},
		data() {
			return {
				swipers:[
					{
						src:"../../static/images/lc250.png",
					},
					{
						src:"../../static/images/wrangler.png"
					},
					{
						src:"../../static/images/goole.png"
					}
				],
				
				iconArray:[
					{
						src:"../../static/indexNav/1.png",
						text:'新品发布'
					},
					{
						src:"../../static/indexNav/2.gif",
						text:'小米众筹'
					},
					{
						src:"../../static/indexNav/3.gif",
						text:'以旧换新'
					},
					{
						src:"../../static/indexNav/4.gif",
						text:'一分拼团'
					},
					{
						src:"../../static/indexNav/5.gif",
						text:'超值特卖'
					},
					{
						src:"../../static/indexNav/6.gif",
						text:'小米秒杀'
					},
					{
						src:"../../static/indexNav/7.gif",
						text:'真心想要'
					},
					{
						src:"../../static/indexNav/8.gif",
						text:'电视特卖'
					},
					{
						src:"../../static/indexNav/9.gif",
						text:'家电热卖'
					},
					{
						src:"../../static/indexNav/10.gif",
						text:'米粉卡'
					},
				],
				threeeAdv:{
					big:{
						src:"../../static/images/demo/demo1.jpg"
					},
					smallTop:{
						src:"../../static/images/demo/demo2.jpg"
					},
					smallBottom:{
						src:"../../static/images/demo/demo3.jpg"
					}
				}
				
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>

</style>