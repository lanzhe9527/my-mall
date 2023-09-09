<template>
	<view style="height: 100%; border-top: 1rpx solid lightgray;box-sizing: border-box;" class="d-flex">
		<scroll-view scroll-y="true" style="flex: 1;border-right: 1rpx solid lightgray;">
			<view class="py-1" style="border-bottom: 1rpx solid lightgray;"
			hover-class="gray-bg-color"
			 v-for="(item,index) in cate" :key="index"
			 @tap="selected(index)">
				<view class="py-1 text-center" :class="activeIndex===index?'slect-active':''">{{item.name}}</view>
			</view>
		</scroll-view>

		<scroll-view scroll-y="true" style="flex: 3.5;">
			<view v-for="(i,index) in 50" :key="index">{{i}}</view>
		</scroll-view>


	</view>
</template>

<script>
	export default {
		data() {
			return {
				activeIndex:0,
				cate: [],
			}
		},
		onLoad() {
			for (let i = 1; i < 20; i++) {
				this.cate.push({
					name: '分类' + i
				})
			}
		},
		methods: {
			selected(index){
				this.activeIndex=index
			}
		}
	}
</script>

<style scoped>
	.slect-active {
		border-left: 8rpx solid #fd6801;
		color: #fd6801;
	}
</style>