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
				}]
			}
		},
		methods: {

		}
	}
</script>

<style scoped>

</style>