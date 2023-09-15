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
			<!-- 外620x380
				头像70
				图片高115 -->
			<view class="px-2 py-2">
				<scroll-view scroll-x="true" scroll-y="false" class="scroll-row">
					<view class="scroll-row-item bg-gray ridus mr-2 px-2 py-2" style="width: 620rpx;height: 380rpx;">
						<view class="d-flex a-center">
							<view class="d-flex a-center">
								<image src="../../static/images/demo/demo6.jpg" class="mr-2" style="width: 70rpx;height: 70rpx; border-radius: 50%;"></image>
								<view class="d-flex flex-column text-gray line-h-md">
									<text>大师兄</text>
									<text>2023-09-12</text>
								</view>
							</view>
							<view style="margin-left: auto;">
								<view class="iconfont icon-dianzan text-gray">164</view>
							</view>
						</view>
						<view class="mt-2">评论支持好评评论支持好评评论</view>
						<view class="d-flex mt-4">
							<view class="span24-8 px-3">
								<image src="../../static/images/demo/demo6.jpg" style="height: 115rpx;"></image>
							</view>
							<view class="span24-8 px-2">
								<image src="../../static/images/demo/demo6.jpg" style="height: 115rpx;"></image>
							</view>
							<view class="span24-8 px-2">
								<image src="../../static/images/demo/demo6.jpg" style="height: 115rpx;"></image>
							</view>
						</view>
					</view>
					
					<view class="scroll-row-item bg-gray ridus mr-2 px-2 py-2" style="width: 620rpx;height: 380rpx;">
						<view class="d-flex a-center">
							<view class="d-flex a-center">
								<image src="../../static/images/demo/demo6.jpg" class="mr-2" style="width: 70rpx;height: 70rpx; border-radius: 50%;"></image>
								<view class="d-flex flex-column text-gray line-h-md">
									<text>大师兄</text>
									<text>2023-09-12</text>
								</view>
							</view>
							<view style="margin-left: auto;">
								<view class="iconfont icon-dianzan text-gray">164</view>
							</view>
						</view>
						<view class="mt-2">评论支持好评评论支持好评评论</view>
						<view class="d-flex mt-4">
							<view class="span24-8 px-3">
								<image src="../../static/images/demo/demo6.jpg" style="height: 115rpx;"></image>
							</view>
							<view class="span24-8 px-2">
								<image src="../../static/images/demo/demo6.jpg" style="height: 115rpx;"></image>
							</view>
							<view class="span24-8 px-2">
								<image src="../../static/images/demo/demo6.jpg" style="height: 115rpx;"></image>
							</view>
						</view>
					</view>
					
				
				</scroll-view>
			</view>



	</view>
</template>

<script>
	import swiperImage from "@/components/index/swiper-images.vue"
	import baseInfo from "@/components/detail/base-info.vue"
	import scrollAttrs from "@/components/detail/scroll-attrs.vue"
	export default {
		components: {
			swiperImage,
			baseInfo,
			scrollAttrs,
		},
		data() {
			return {
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