<template>
	<view class="">
		<!-- 外620x380
			头像70
			图片高115 -->
		<view class="px-2 py-2">
			<scroll-view scroll-x="true" scroll-y="false" class="scroll-row">
				<view class="scroll-row-item bg-gray ridus mr-2 px-2 py-2" 
				style="width: 620rpx;height: 380rpx;" v-for="(item,index) in comments" :key="index">
					<view class="d-flex a-center">
						<view class="d-flex a-center">
							<image :src="item.userpic" class="mr-2" style="width: 70rpx;height: 70rpx; border-radius: 50%;"></image>
							<view class="d-flex flex-column text-gray line-h-md">
								<text>{{item.username}}</text>
								<text>{{item.create_time}}</text>
							</view>
						</view>
						<view style="margin-left: auto;">
							<view class="iconfont icon-dianzan text-gray">{{item.goods_num}}</view>
						</view>
					</view>
					<view class="mt-2">{{item.context}}</view>
					<view class="d-flex mt-4">
						<view class="span24-8 px-3" v-for="(item1,index) in item.imgList" :key="index">
							<image :src="item1" style="height: 115rpx;"></image>
						</view>
						
					</view>
				</view>
			</scroll-view>
		</view>
		
		
		<view class="d-flex j-center a-center">
			<text class="mr-1">更多评论</text>
			<i class="iconfont icon-jiantouyou"></i>
		</view>
	</view>
	
	
</template>

<script>
	export default{
		props:{
			comments:Array
			
		}
	}
</script>

<style>
</style>