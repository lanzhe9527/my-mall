<template>
	<view>
		<!-- 首页分类 -->
		<view class="index-class-box">
			<block v-for="(item,index) in iconNav">
			<view class="span-box">
				<image :src="item.src" style="width: 60rpx; height: 60rpx;"></image>
			<text>{{item.text}}</text>
			</view>
			</block>
		</view>
	</view>
</template>

<script>
	export default{
		props:{
			iconNav:Array
		}
	}
</script>

<style>
	.index-class-box{
		display: flex;
		flex-wrap: wrap;
		padding: 20rpx;
	}
	.span-box{
		width: 20%;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding:20rpx 0;
	
	}
</style>