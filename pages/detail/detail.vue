<template>
	<view>
		<!-- 商品详情大图 -->
		<swiper-image :resdata="banner" height="750"></swiper-image>
		<!-- 基础详情 -->
		<base-info :detail="detail"></base-info>
		<!-- 滚动商品特性 170x110-->
		<scroll-attrs :baseAttrs="baseAttrs"></scroll-attrs>
		
		<view class="px-2 py-2">
			<view class="gray-bg-color">
				<ui-list>
					<uni-list-item showArrow :customStyle="{ backgroundColor: '#F1F1F1',padding:''}">
						<view class="font-md">
							<text class="mr-2">已选</text>
							<text>火焰红 64GB 标配</text>
						</view>
					</uni-list-item>
					
					<uni-list-item showArrow :customStyle="{ backgroundColor: '#F1F1F1',padding:''}">
						<view class="font-md">
							<text class="mr-2">配送</text>
							<text class="mr-2">北京 东城区</text>
							<text class="main-text-color">有现货</text>
						</view>
					</uni-list-item>
					
					<uni-list-item showArrow :customStyle="{ backgroundColor: '#F1F1F1',padding:''}">
						<view class="font-md d-flex">
							<view class="mr-3">
								<i class="iconfont icon-check main-text-color mr-1"></i>
								<text>小米自营</text>
							</view>
							<view class="mr-3">
								<i class="iconfont icon-check main-text-color mr-1"></i>
								<text>小米自营</text>
							</view>
							<view class="mr-3">
								<i class="iconfont icon-check main-text-color mr-1"></i>
								<text>小米自营</text>
							</view>
							
						</view>
					</uni-list-item>
				</ui-list>
			</view>
		</view>
			<!-- 横向滚动评论 -->
			
			<scroll-comments :comments="comments"></scroll-comments>
			
		
	</view>
</template>

<script>
	import swiperImage from "@/components/index/swiper-images.vue"
	import baseInfo from "@/components/detail/base-info.vue"
	import scrollAttrs from "@/components/detail/scroll-attrs.vue"
	import scrollComments from "@/components/detail/scroll-comments.vue"
	export default {
		components: {
			swiperImage,
			baseInfo,
			scrollAttrs,
			scrollComments,
		},
		data() {
			return {
				// 评论
				comments:[{
					userpic:"../../static/images/demo/demo6.jpg",	
					username:"大师兄",	
					create_time:"2023-09-12",	
					goods_num:"189",	
					context:"评论支持好评评论支持好评评论",	
					imgList:[
						"../../static/images/demo/demo6.jpg",
						"../../static/images/demo/demo6.jpg",
						"../../static/images/demo/demo6.jpg",
					]
				},{
					userpic:"../../static/images/demo/demo6.jpg",	
					username:"大师兄",	
					create_time:"2023-09-12",	
					goods_num:"189",	
					context:"评论支持好评评论支持好评评论",	
					imgList:[
						"../../static/images/demo/demo6.jpg",
						"../../static/images/demo/demo6.jpg",
						"../../static/images/demo/demo6.jpg",
					]
				}],
				
				
				banner: [{
					src: "https://cdn.cnbj0.fds.api.mi-img.com/b2c-shopapi-pms/pms_1679982565.14646441.png"
				}, {
					src: "https://cdn.cnbj0.fds.api.mi-img.com/b2c-shopapi-pms/pms_1681805069.68642151.png"
				}, {
					src: "https://cdn.cnbj0.fds.api.mi-img.com/b2c-shopapi-pms/pms_1692003918.717685.jpg"
				}],
				detail:{
					title:"小米mix3 6GB+128GB",
					desc:"磁动力滑盖全面屏 / 前后旗舰AI双摄 / 高效100W无线充电 / 彩色陶瓷机身",
					pPrice:"4899"
				},
				baseAttrs:[
					{icon:"icon-cpuchuliqiyingjian",title:"cpu",desc:"蛟龙888处理器"},
					{icon:"icon-cpuchuliqiyingjian",title:"cpu",desc:"蛟龙888处理器"},
					{icon:"icon-cpuchuliqiyingjian",title:"cpu",desc:"蛟龙888处理器"},
					{icon:"icon-cpuchuliqiyingjian",title:"cpu",desc:"蛟龙888处理器"},
					{icon:"icon-cpuchuliqiyingjian",title:"cpu",desc:"蛟龙888处理器"},
					{icon:"icon-cpuchuliqiyingjian",title:"cpu",desc:"蛟龙888处理器"},
					{icon:"icon-cpuchuliqiyingjian",title:"cpu",desc:"蛟龙888处理器"},
					{icon:"icon-cpuchuliqiyingjian",title:"cpu",desc:"蛟龙888处理器"},
					
				],
				
			}
		},
		methods: {

		}
	}
</script>

<style scoped>

</style>