<template>
	<view>
		<!-- 商品详情大图 -->
		<swiper-image :resdata="banner" height="750"></swiper-image>
	</view>
</template>

<script>
	import swiperImage from "@/components/index/swiper-images.vue"
	export default {
		components: {
			swiperImage,
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

<style>

</style>