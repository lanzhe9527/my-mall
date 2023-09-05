<template>
	<view class="card-box">
		<!-- 标题 -->
		<view class="title-box">
			<text class="title-text">{{headerTitle}}</text>
		</view>
		<image :src="bodyImg" mode="widthFix" v-if="bodyImg"
		style="width: 750rpx;height: 300rpx;">
		</image>
		<slot />
	</view>
</template>

<script>
	export default{
		props:{
			headerTitle:String,
			bodyImg:String,
			// 是否显示头部
			showhead:{
				type:Boolean,
				default:true
			}
		}
	}
</script>

<style scoped>
	.title-box {
		border-bottom: 1rpx solid #f1f1f1;
		padding: 10rpx 20rpx;

	}

	.title-text {
		font-size: 30rpx;
		font-weight: 500;
	}
</style>