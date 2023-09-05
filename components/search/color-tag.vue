<template>
		<view class="button" :style="getBgStyle">{{item.name}}</view>
</template>

<script>
	export default{
		props:{
			item:Object,
			
		},
		computed: {
			getBgStyle() {
				let color = {
					borderColor: ['#ff88c2', '#00aa88', '#0066ff', '#b94fff', '#aaaaaa', '#ffcc22', '#ff8800'],
					backgroundColor: ['#ffb7dd', '#00ddaa', '#5599ff', '#d28fff', '#dddddd', '#ffdd55', '#ffaa33'],
				}
				let index = Math.floor(Math.random() * color.borderColor.length)
				let borderColor = color.borderColor[index]
				let backgroundColor = color.backgroundColor[index]
				return `borderColor:${borderColor};backgroundColor:${backgroundColor}`
			}
		},
	}
</script>

<style scoped>
	.button-box {
		padding: 10px;
	}
	
	.button {
		display: inline-block;
		padding: 2px 10px;
		border: 2px solid lightgray;
		margin: 5px 10px;
	}
</style>