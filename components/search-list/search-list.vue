<template>
	<view>
		<view class="px-2 py-2 d-flex" style="border-bottom: 1rpx solid lightgray;align-items: center;"
		v-for="(item,index) in list" :key="index">
			<view class="" style="width: 320rpx;">
				<image :src="item.titlePic" mode="widthFix" style="width: 100%;"></image>
			</view>
			<view class="" style="margin-left: 20rpx;">
				<view class="" style="font-weight: 500;font-size: 34rpx;">{{item.title}}</view>
				<view class="text-gray" style="line-height: 40rpx;margin-bottom: 20rpx;">{{item.desc}}</view>
				<price style="font-weight: 500;">{{item.pprice}}</price>
				<view class="">{{item.comment_num}}条评论 {{item.good_num}}满意</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		props:{
			list:Array
		}
		
	}
</script>

<style>
</style>