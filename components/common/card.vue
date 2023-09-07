<template>
	<view class="card-box">
		<!-- 标题 -->
		<view class="title-box" :class="getHeaderClass">
			<text class="title-text" :class="fontWeight?'font-weight':''">{{headerTitle}}</text>
		</view>
		<image :src="bodyImg" mode="widthFix" v-if="bodyImg" style="width: 750rpx;height: 300rpx;">
		</image>
		<slot />
	</view>
</template>

<script>
	export default {
		props: {
			headerTitle: String,
			bodyImg: String,
			// 是否显示头部
			showhead: {
				type: Boolean,
				default: true
			},
			// 文字是否加粗
			fontWeight: {
				type: Boolean,
				default: true
			},
			// 是否显示下边线
			borderBottom: {
				type: Boolean,
				default: true
			},

		},
		computed: {
			getHeaderClass() {
				let rz = this.borderBottom ? 'border-bottom' : ''
				return `${rz}`
			}
		}
	}
</script>

<style scoped>
	.title-box {
		padding: 10rpx 20rpx;

	}

	.title-text {
		font-size: 30rpx;
	}

	.border-bottom {
		border-bottom: 1rpx solid lightgray;
	}

	.font-weight {
		font-weight: 500;
	}

	.color {
		color: red;
	}
</style>