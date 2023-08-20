<template>
	<view>
		<!-- 轮播图 -->
		<swiper indicator-dots autoplay :interval="3000" :duration="1000" indicator-color="gray"
				indicator-active-color="#FFF" circular>
				<block v-for="(item,index) in swipers" :key="index">
					<swiper-item>
						<view class="swiper-item">
							<image :src="item.src" style="height: 350rpx;"></image>
						</view>
					</swiper-item>
				</block>
		</swiper>

		
		
		
	</view>
</template>

<script>
	export default {
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