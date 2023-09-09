<template>
	<view style="height: 100%; border-top: 1rpx solid lightgray;box-sizing: border-box;" class="d-flex">
		<scroll-view scroll-y="true" style="flex: 1;border-right: 1rpx solid lightgray;">
			<view class="py-1" style="border-bottom: 1rpx solid lightgray;" hover-class="gray-bg-color"
				v-for="(item,index) in cate" :key="index" @tap="selected(index)">
				<view class="py-1 text-center" :class="activeIndex===index?'slect-active':''">{{item.name}}</view>
			</view>
		</scroll-view>

		<scroll-view scroll-y="true" style="flex: 3.5;">
			<view class="d-flex" style="flex-wrap: wrap;" v-for="(item,index) in list" :key="index">
				<view class="span24-8 py-2 text-center" v-for="(item2,index2) in item.list" :key="index2">
					<image :src="item2.src" mode="" style="width: 120rpx;height: 120rpx;">
					</image>
					<view class="">{{item2.name}}</view>
				</view>


			</view>
		</scroll-view>


	</view>
</template>

<script>
	export default {
		data() {
			return {
				activeIndex: 0,
				cate: [],
				list: [],
			}
		},
		onLoad() {
			this.getData()
		},
		methods: {
			selected(index) {
				this.activeIndex = index
			},
			getData() {
				for (let i = 1; i < 20; i++) {
					this.cate.push({
						name: '分类' + i
					})
					this.list.push({
						list: []
					})
				}

				for (let i = 0; i < this.list.length; i++) {
					for (let j = 0; j < 10; j++) {
						this.list[i].list.push({
							src: "../../static/images/demo/cate_07.png",
							name:`分类${i}-商品${j}`
						})
					}
				}
				
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