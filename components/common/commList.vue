<template>
	<view class="commList-box" style="display: flex;flex-wrap: wrap;justify-content: space-between;">
	<block v-for="(item,index) in commonList" :key="index">
		<view class="" style="width: 372rpx;display: flex; flex-direction: column;">
		<image :src="item.cover" mode="widthFix"></image>
		<view class="" style="padding: 10rpx 30rpx;display: flex;flex-direction: column;">
			<text style="font-size: 30rpx;">{{item.title}}</text>
			<text style="color: darkgray;">{{item.desc}}</text>
			<view class="" style="display: flex;">
				<price>{{item.nPrice}}</price>
				<text style="margin-left: 30rpx;font-size: 25rpx;
							text-decoration: line-through;
							align-self: flex-end;color: darkgray;">¥{{item.oPrice}}</text>
			</view>
			</view>
		</view>
	</block>
	</view>
</template>

<script>
	import price from "@/components/common/price.vue"
	export default{
		components:{
			price
		},
		props:{
			commonList:Array
		}
	}
</script>

<style>
</style>