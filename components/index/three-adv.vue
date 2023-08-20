<template>
	<view class="adv-box">
		<image :src="advdata.big.src" class="big-img" @tap="event(advdata.big)"></image>
		<view class="small-adv-box">
			<image :src="advdata.smallTop.src" class="small-img small-pd" @tap="event(advdata.smallTop)"></image>
			<image :src="advdata.smallBottom.src" class="small-img" @tap="event(advdata.smallBottom)"></image>

		</view>
	</view>
</template>

<script>
	export default{
		props:{
			advdata:Object
		},
		methods:{
			event(obj){
				console.log(obj)
			}
		}
	}
</script>

<style>
	.adv-box {
		display: flex;
	}

	.big-img {
		width: 373upx;
		height: 530rpx;
		border-right: 2rpx solid #f5f5f5;
	}

	.small-adv-box {
		display: flex;
		flex-direction: column;
	}
	.small-img{
		width: 375rpx;height: 264rpx; 
	}
	.small-pd{
		border-bottom: 2rpx solid #f5f5f5;
	}
</style>