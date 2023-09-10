<template>
	<view style="height: 100%; border-top: 1rpx solid lightgray;box-sizing: border-box;" class="d-flex">
		<scroll-view scroll-y="true" style="flex: 1;border-right: 1rpx solid lightgray;">
			<view class="py-1 left-scroll-item" style="border-bottom: 1rpx solid lightgray;" hover-class="gray-bg-color"
				v-for="(item,index) in cate" :key="index" @tap="selected(index)">
				<view class="py-1 text-center" :class="activeIndex===index?'slect-active':''">{{item.name}}</view>
			</view>
		</scroll-view>

		<scroll-view scroll-y="true" style="flex: 3.5;" :scroll-top="rightScrollTop" :scroll-with-animation="true"
			@scroll="onRightScroll">
			<view class="d-flex right-scroll-item" style="flex-wrap: wrap;" v-for="(item,index) in list" :key="index">
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
				leftDomsTop: [],
				rightDomsTop: [],
				rightScrollTop: 0,
			}
		},
		onLoad() {
			this.getData()
		},
		onReady() {
			const query = uni.createSelectorQuery().in(this);
			const query1 = uni.createSelectorQuery().in(this);
			query.selectAll('.left-scroll-item').boundingClientRect(data => {
				console.log(data)
				this.leftDomsTop = data.map(v => {
					return v.top
				})
				console.log(this.leftDomsTop)
			}).exec();

			query1.selectAll('.right-scroll-item').boundingClientRect(data => {
				console.log(data)
				this.rightDomsTop = data.map(v => {
					return v.top
				})
				console.log(this.rightDomsTop)
			}).exec();

		},
		methods: {
			selected(index) {
				this.activeIndex = index
				this.rightScrollTop = this.rightDomsTop[index]
			},
			// 监听右边滚动事件
			onRightScroll(e) {
				console.log(e.detail.scrollTop)
				// 匹配当前scrollTop所处索引
				this.rightDomsTop.forEach((v, k) => {
					if (v<e.detail.scrollTop) {
						this.activeIndex=k
						return false
					}
				})
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
							name: `分类${i+1}-商品${j}`
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