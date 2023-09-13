<template>
	<view class="main-text-color prcie-box" :class="priceSize">
		<text class="price-icon" :class="unitSize">¥</text><slot/>
	</view>
</template>

<script>
	export default {
		props:{
			unitSize:{
				type:String,
				default:"font-sm"
			},
			priceSize:{
				type:String,
				default:"font-md"
			}
		}
	}
</script>

<style>
	.prcie-box {
		display: flex;
	}

	.price-icon {
		align-self: flex-start;
		margin-right: 5rpx;
	}
</style>