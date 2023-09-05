<template>
	<view>
		<card headerTitle="热门搜索" body-img="../../static/images/demo/cate_banner.png"></card>
		<!-- 多色按钮 -->
		<view class="button-box">
				<color-tag :item="item" v-for="(item,index) in hot" :key="index"></color-tag>
		</view>
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
				]
			}
		},
	
		methods: {

		}
	}
</script>

<style>
	
</style>