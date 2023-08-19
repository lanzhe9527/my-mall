<template>
	<view>
		<!-- 轮播图 -->
		<swiper indicator-dots autoplay :interval="3000" :duration="1000">
			<swiper-item>
				<view class="swiper-item" style="background-color: aqua;">
					<image src="../../static/images/lc250.png" style="height: 350rpx;"></image>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item" style="background-color: bisque;">2</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item" style="background-color: bisque;">3</view>
			</swiper-item>
		</swiper>
	</view>
	
	
	
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
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