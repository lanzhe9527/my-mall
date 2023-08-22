<template>
	<view>
		<!-- 轮播图 -->
		<swiper-images :resdata="swipers"></swiper-images>
		<!-- 首页分类 -->
		<nav-icon :iconNav="iconArray"></nav-icon>
		<!-- 全局分割线 -->
		<divider></divider>
		<!-- 三图广告 -->
		<three-adv :advdata="threeeAdv"></three-adv>
		
		<!-- 全局分割线 -->
		<divider></divider>
		<!-- 每日推荐 -->
		<card headerTitle="每日推荐" bodyImg="/static/images/demo/demo8.jpg"></card>
		
		<!-- 列表 -->
		<common-list :commonList="commonList"></common-list>
		
		
		
	</view>
</template>

<script>
	import swiperImages from "@/components/index/swiper-images.vue"
	import navIcon from "@/components/index/index-nav.vue"
	import threeAdv from "@/components/index/three-adv.vue"
	import card from "@/components/common/card.vue"
	import commonList from "@/components/common/commList.vue"
	export default {
		components:{
			swiperImages,
			navIcon,
			threeAdv,
			card,
			commonList
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
				},
				commonList:[
					{
						cover:"../../static/images/list/1.jpg",
						title:"米家空调",
						desc:"1.5匹变流空调",
						oPrice:"2678",
						nPrice:"1999"
					},
					{
						cover:"../../static/images/list/2.jpg",
						title:"黑鲨手机",
						desc:"游戏性能，散热好",
						oPrice:"2678",
						nPrice:"1299"
					},
					{
						cover:"../../static/images/list/3.jpg",
						title:"红米手机",
						desc:"1.5匹变流空调",
						oPrice:"2678",
						nPrice:"1999"
					},
					{
						cover:"../../static/images/list/4.jpg",
						title:"荣耀",
						desc:"1.5匹变流空调",
						oPrice:"2678",
						nPrice:"1999"
					},
					{
						cover:"../../static/images/list/5.jpg",
						title:"红米redmi",
						desc:"1.5匹变流空调",
						oPrice:"2678",
						nPrice:"1999"
					},
					{
						cover:"../../static/images/list/6.jpg",
						title:"米家平板",
						desc:"本地数据",
						oPrice:"2678",
						nPrice:"1999"
					}
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