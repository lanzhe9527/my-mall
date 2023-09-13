<template>
	<view>
		<!-- 商品详情大图 -->
		<swiper-image :resdata="banner" height="750"></swiper-image>
		<!-- 基础详情 -->
		<view class="px-2">
			<view class="font-lg">小米MIX</view>
			<view class="font-md text-gray line-h-sm mb-3">次动力次动力次动力次动力次动力次动力次动力次动力次动力</view>
			<price price-size="font-lg" unit-size="font">3199</price>
		</view>
		<!-- 滚动商品特性 170x110-->
		<scroll-view scroll-x="true" class="scroll-row">
			<view class="scroll-row-item" style="width: 170rpx;height:110rpx;" 
				v-for="(item,index) in baseAttrs" :key="index">
				<view class="d-flex flex-column a-center j-center" style="height:110rpx;">
					<view class="line-h-sm iconfont" :class="item.icon"></view>
					<view class="line-h">{{item.title}}</view>
					<view class="font-sm text-gray">{{item.desc}}</view>
				</view>
			</view>

		</scroll-view>





	</view>
</template>

<script>
	import swiperImage from "@/components/index/swiper-images.vue"
	import price from "@/components/common/price.vue"
	export default {
		components: {
			swiperImage,
			price,
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