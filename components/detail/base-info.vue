<template>
	<view>
		<view class="px-2">
			<view class="font-lg">{{detail.title}}</view>
			<view class="font-md text-gray line-h-sm mb-3">{{detail.desc}}</view>
			<price price-size="font-lg" unit-size="font">{{detail.pPrice}}</price>
		</view>
	</view>
</template>

<script>
	import price from "@/components/common/price.vue"
	export default {
		components: {
			price
		},
		props: ['detail']
	}
</script>

<style>
</style>