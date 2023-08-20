<template>
	<view>
		<!-- 轮播图 -->
		<swiper-images :resdata="swipers"></swiper-images>
		<!-- 首页分类 -->
		<nav-icon :iconNav="iconArray"></nav-icon>
		
		
	</view>
</template>

<script>
	import swiperImages from "@/components/index/swiper-images.vue"
	import navIcon from "@/components/index/index-nav.vue"
	export default {
		components:{
			swiperImages,
			navIcon
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
				]
				
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