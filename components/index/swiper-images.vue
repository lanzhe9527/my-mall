<template>
	<view>
		<!-- 轮播图 -->
		<swiper indicator-dots autoplay :interval="3000" :duration="1000" indicator-color="gray"
				indicator-active-color="#FFF" circular>
				<block v-for="(item,index) in resdata" :key="index">
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
	export default{
		props:{
			resdata:Array
		}
	}
</script>

<style>
</style>