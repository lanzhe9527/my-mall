<template>
	<view>
		<!-- 轮播图 -->
		<swiper indicator-dots autoplay :interval="3000" :duration="1000" indicator-color="gray"
				indicator-active-color="#FFF" circular :style="getStyle">
				<block v-for="(item,index) in resdata" :key="index">
					<swiper-item>
						<view class="swiper-item">
							<image :src="item.src" :style="getStyle"></image>
						</view>
					</swiper-item>
				</block>
		</swiper>
	</view>
</template>

<script>
	export default{
		props:{
			resdata:Array,
			height:{
				type:String,
				default:"350rpx"
			},
		},
		computed:{
			getStyle(){
			return `height: ${this.height}rpx;`	
			}
		},
		
	}
</script>

<style>
</style>