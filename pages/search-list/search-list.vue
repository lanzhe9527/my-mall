<template>
	<view>
		<!-- 	<text class="iconfont icon-shengxu"></text> -->

		<view class="list-tab-box">
			<view class="list-tab-item" v-for="(item,index) in screen.list" @tap="changeScreen(index)">
				<text :class="screen.currentIndex===index? 'main-text-color':'' ">{{item.name}}</text>
				<view class="icon-box">
					<i class="iconfont icon-shengxu l-height-0" :class="item.status===1? 'main-text-color':''"></i>
					<i class="iconfont icon-jiangxu l-height-0" :class="item.status===2? 'main-text-color':''"></i>
				</view>
			</view>

			<view class="list-tab-item" @click="showDrawer">
				<text class="main-text-color">筛选</text>
			</view>
		</view>
		<!-- 抽屉 -->
		<uni-drawer mode="right" ref="showRight" :width="310">
			<card headerTitle="服务" :fontWeight="false" :borderBottom="false">
				<view class="d-flex">
					<view class="span24-8 px-2" v-for="(item,index) in label.list" :key="index">
						<view class="ridus text-center px-2 py-1 font-md bg-gray"
						:class="label.seleced===index?'radio-active':'radio-border'"
						@tap="tapSlect(index)">{{item.name}}</view>
					</view>
				</view>
			</card>
			<!-- 底部按钮 -->
			<view class="bt-box">
				<view class="bt text-write main-bg-color">确定</view>
				<view class="bt gray-bg-color">重置</view>
			</view>
		</uni-drawer>


	</view>
</template>

<script>
	import card from "@/components/common/card.vue"
	export default {
		components: {
			card,
		},
		data() {
			return {
				screen: {
					currentIndex: 0,
					list: [{
							name: "综合",
							status: 1
						},
						{
							name: "销量",
							status: 0
						},
						{
							name: "价格",
							status: 0
						}
					]
				},
				label: {
					seleced: 0,
					list: [{
							name: '选项一'
						},
						{
							name: '选项二'
						},
						{
							name: '选项三'
						}
					]

				}
			}
		},
		methods: {
			changeScreen(index) {
				// 判断当前点击是否已激活
				let oldIndex = this.screen.currentIndex
				let oldItem = this.screen.list[oldIndex]
				if (oldIndex === index) {
					return oldItem.status = oldItem.status === 1 ? 2 : 1
				}
				let newItem = this.screen.list[index]
				this.screen.currentIndex = index
				oldItem.status = 0
				newItem.status = 1

			},
			// 抽屉
			showDrawer() {
				this.$refs.showRight.open();
			},
			tapSlect(index){
				this.label.seleced=index
			}
		},
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

	/* 抽屉 */

	.bt-box {
		position: fixed;
		bottom: 0;
		right: 0;
		width: 100%;
		display: flex;
		border-top: 1px solid lightgray;
		border-bottom: 1px solid lightgray;
	}

	.bt {
		flex: 1;
		padding: 20rpx;
		text-align: center;
	}

	.radio-active {
		color: #eb7320 !important;
		background-color: #fce0d5 !important;
		border-color: #eb7320 !important;
	}

	.radio-border {
		border: 1rpx solid #f1f1f1;
	}
</style>