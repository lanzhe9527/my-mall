<template>
	<view>
		<!-- 	<text class="iconfont icon-shengxu"></text> -->

		<view class="list-tab-box">
			<view class="list-tab-item">
				<text class="main-text-color">综合</text>
				<view class="icon-box">
					<i class="iconfont icon-shengxu l-height-0 main-text-color"></i>
					<i class="iconfont icon-jiangxu l-height-0"></i>
				</view>
			</view>

			<view class="list-tab-item">
				<text>销量</text>
				<view class="icon-box">
					<i class="iconfont icon-shengxu l-height-0"></i>
					<i class="iconfont icon-jiangxu l-height-0"></i>
				</view>
			</view>

			<view class="list-tab-item">
				<text>价格</text>
				<view class="icon-box">
					<i class="iconfont icon-shengxu l-height-0"></i>
					<i class="iconfont icon-jiangxu l-height-0"></i>
				</view>
			</view>

			<view class="list-tab-item">
				<text class="main-text-color">筛选</text>
			</view>

		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {

		}
	}
</script>

<style scoped>
	.list-tab-box {
		height: 100rpx;
		display: flex;
		border-top: 1rpx solid lightgray;
		border-bottom: 1rpx solid lightgray;
	}

	.list-tab-item {
		flex: 1;
		display: flex;
		justify-content: center;
		align-items: center;
		color: #8f8f94;
	}


	.icon-box {
		display: flex;
		flex-direction: column;
	}

	.l-height-0 {
		line-height: 0.7;
		font-size: 20rpx;
	}
</style>