<template>
	<view class="d-flex">
		<view class="span24-8 px-2" v-for="(item,index) in label.list" :key="index">
			<view class="ridus text-center px-2 py-1 font-md bg-gray"
			:class="label.seleced===index?'radio-active':'radio-border'"
			@tap="tapSlect(index)">{{item.name}}</view>
		</view>
	</view>
</template>

<script>
	export default{
		props:{
			label:Object
		},
		methods:{
			tapSlect(index){
				// this.$emit('change',index)
				this.$emit('update:seleced',index)
			}
		}
	}
	
</script>

<style scoped>
	.radio-active {
		color: #eb7320 !important;
		background-color: #fce0d5 !important;
		border-color: #eb7320 !important;
	}
	
	.radio-border {
		border: 1rpx solid #f1f1f1;
	}
</style>