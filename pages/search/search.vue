<template>
	<view>
		<card headerTitle="热门搜索" body-img="../../static/images/demo/cate_banner.png"></card>
		<!-- 多色按钮 -->
		<view class="button-box">
				<color-tag :item="item" v-for="(item,index) in hot" :key="index"></color-tag>
		</view>
		<!-- 常用分类 -->
		<card header-title="常用分类">
			<color-tag :item="item" v-for="(item,index) in cate" :key="index" :color="false"></color-tag>
		</card>
		
		<card header-title="搜索记录">
			<uni-list-item title="小米"></uni-list-item>
			<uni-list-item title="小米"></uni-list-item>
			<uni-list-item title="小米"></uni-list-item>
			<uni-list-item title="小米"></uni-list-item>
		</card>
		
	</view>
</template>

<script>
	import card from "@/components/common/card.vue"
	import colorTag from "@/components/search/color-tag.vue"
	export default {
		components: {
			card,
			colorTag,
		},
		data() {
			return {
				hot:[
					{name:'领券中心'},
					{name:'LC250越野车'},
					{name:'Jeep牧马人'},
					{name:'tank500Hi4-t'},
					{name:'福特猛禽烈马'},
				],
				cate:[
					{name:'耳机充电座'},
					{name:'手机'},
					{name:'电脑/电脑'},
					{name:'箱包'},
					{name:'手表带'},
					{name:'酷玩'},
				]
			}
		},
		onNavigationBarButtonTap(e) {
			console.log(e.index)
			if (e.index===0) {
				uni.navigateTo({
					url:'/pages/search-list/search-list'
				})
			}
		},
		methods: {

		}
	}
</script>

<style>
	
</style>