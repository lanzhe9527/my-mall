<template>
	<view class="main-text-color prcie-box">
		<text class="price-icon">¥</text>{{price}}
	</view>
</template>

<script>
	export default {
		props: {
			price: [String, Number]
		}
	}
</script>

<style>
	.prcie-box {
		display: flex;
	}

	.price-icon {
		align-self: flex-start;
		font-size: 22rpx;
		margin-right: 5rpx;
	}
</style>