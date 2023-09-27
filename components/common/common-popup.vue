<template>
	<view class="_popup" :class="popupClass">
		<view class="_mask" @tap.stop='hide'></view>
		<view class="_body">内容</view>
	</view>
</template>

<script>
	export default{
		props:{
			popupClass:{
				type:String,
				default:'none'
			}
		},
		methods:{
			hide(){
				this.$emit('hide')
			}
		}
	}
</script>

<style scoped>
	._popup,._mask{
		position: fixed;
		top: 0;
		width: 100%;
		height: 100%;
	}
	
	._popup{
		z-index: 2000;
	}
	
	._mask{
		z-index: 2001;
		background-color: rgba(0, 0, 0, 0.5);
	}
	._body{
		z-index: 2002;
		background-color: #fff;
		position: fixed;
		bottom: -1035rpx;
		width: 92%;
		height: 1035rpx;
		padding: 0 4%;
		border-radius: 20rpx 20rpx 0 0;
	}
	
	@keyframes showBody{
		0%{transform: translateY(0);}
		100%{transform: translateY(-100%)}
	}
	@keyframes hideBody{
		0%{transform: translateY(-100%);}
		100%{transform: translateY(0)}
	}
	@keyframes showMask{
		0%{opacity: 0;}
		100%{opacity: 1;}
	}
	@keyframes hideMask{
		0%{opacity: 1;}
		100%{opacity: 0;}
	}
	
	.show{
		display: block;
	}
	.show ._mask{
		animation: showMask 0.2s linear both;
	}
	.show ._body{
		animation: showBody 0.2s linear both;
	}
	.hide{
		display: block;
	}
	.hide ._body{
		animation: hideBody 0.2s linear both;
	}
	.hide ._mask{
		animation: hideMask 0.2s linear both;
	}
	.none{
		display: none;
	}
</style>