<template>
	<view>
		<!-- 轮播图 -->
		<swiper-images :resdata="swipers"></swiper-images>
		
		
		
	</view>
</template>

<script>
	import swiperImages from "@/components/index/swiper-images.vue"
	export default {
		components:{
			swiperImages
		},
		data() {
			return {
				swipers:[
					{
						src:"../../static/images/lc250.png"
					},
					{
						src:"../../static/images/wrangler.png"
					},
					{
						src:"../../static/images/goole.png"
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