<template>
	<view class="card-box">
		<!-- 标题 -->
		<view class="title-box">
			<text class="title-text">{{headerTitle}}</text>
		</view>
		<image :src="bodyImg" mode="widthFix"></image>
	</view>
</template>

<script>
	export default{
		props:{
			headerTitle:String,
			bodyImg:String
		}
	}
</script>

<style>
	.title-box {
		border-bottom: 1rpx solid #f1f1f1;
		padding: 10rpx 20rpx;

	}

	.title-text {
		font-size: 30rpx;
		font-weight: 500;
	}
</style>