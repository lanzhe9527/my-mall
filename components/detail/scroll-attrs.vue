<template>
	<view>
		<scroll-view scroll-x="true" class="scroll-row">
			<view class="scroll-row-item" style="width: 170rpx;height:110rpx;" v-for="(item,index) in baseAttrs"
				:key="index">
				<view class="d-flex flex-column a-center j-center" style="height:110rpx;">
					<view class="line-h-sm iconfont" :class="item.icon"></view>
					<view class="line-h">{{item.title}}</view>
					<view class="font-sm text-gray">{{item.desc}}</view>
				</view>
			</view>
		</scroll-view>

	</view>
</template>

<script>
	export default{
		props:['baseAttrs']
	}
</script>

<style>
</style>