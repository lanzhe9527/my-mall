<template>
	<view>
		<!-- 顶部选项卡 -->
		<scroll-view scroll-x="true" style="white-space: nowrap;height: 80rpx;"
								:scroll-into-view="scrollInto"
								:scroll-with-animation="true">
			<view v-for="(item,index) in tabBars" :key="index" style="display: inline-block;
									padding:0 30rpx;height: 80rpx;line-height: 80rpx; box-sizing: border-box;"
									:class="tabIndex==index? 'bottom-border main-text-color':''" 
									@click="changeTab(index)"
									:id="'tab'+index">
				<text style="font-size: 30rpx;">{{item.name}}</text>
			</view>
		</scroll-view>
		<swiper :current="tabIndex" :style="'height:'+scrollH+'px;'" @change="onChageTab">
			<swiper-item v-for="(item,index) in newsItems" :key="index">
				<scroll-view scroll-y="true" scroll-x="false" :style="'height:'+scrollH+'px;'">
					
					<block v-for="(item1,index1) in item.list" :key="index1">
						
					<!-- 轮播图 -->
					<swiper-images v-if="item1.type==='swiper'" :resdata="item1.data"></swiper-images>
					
					<template v-else-if="item1.type==='iconArray'">
						<!-- 首页分类 -->
						<nav-icon :iconNav="item1.data"></nav-icon>
						<!-- 全局分割线 -->
						<divider></divider>
					</template>
					
					<template  v-else-if="item1.type==='threeeAdv'">
						<!-- 三图广告 -->
						<three-adv :advdata="item1.data"></three-adv>
						
						<!-- 全局分割线 -->
						<divider></divider>
					</template>
					
					
					<!-- 每日推荐 -->
					<!-- <card headerTitle="每日推荐" bodyImg="/static/images/demo/demo8.jpg"></card> -->
					
					<!-- 列表 -->
					<common-list v-else-if="item1.type==='commonList'" :commonList="item1.data"></common-list>
					
					
					</block>
				</scroll-view>
			</swiper-item>
		</swiper>
		

		
		
		
	</view>
</template>

<script>
	// 模拟后端数据
	let demoTabars=[{
						name:"关注"
					},
					{
						name:"推荐"
					},
					{
						name:"体育"
					},
					{
						name:"热点"
					},
					{
						name:"财经"
					},
					{
						name:"军事"
					},
					{
						name:"越野"
					},
					{
						name:"超跑"
					},
					{
						name:"财经"
					},];
					
	let demo1=[{
								type:"swiper",
								data:[
									{
										src:"../../static/images/lc250.png",
									},
									{
										src:"../../static/images/wrangler.png"
									},
									{
										src:"../../static/images/goole.png"
									}
								]
							},
							{
								type:"iconArray",
								data:[
									{
										src:"../../static/indexNav/1.png",
										text:'新品发布'
									},
									{
										src:"../../static/indexNav/2.gif",
										text:'小米众筹'
									},
									{
										src:"../../static/indexNav/3.gif",
										text:'以旧换新'
									},
									{
										src:"../../static/indexNav/4.gif",
										text:'一分拼团'
									},
									{
										src:"../../static/indexNav/5.gif",
										text:'超值特卖'
									},
									{
										src:"../../static/indexNav/6.gif",
										text:'小米秒杀'
									},
									{
										src:"../../static/indexNav/7.gif",
										text:'真心想要'
									},
									{
										src:"../../static/indexNav/8.gif",
										text:'电视特卖'
									},
									{
										src:"../../static/indexNav/9.gif",
										text:'家电热卖'
									},
									{
										src:"../../static/indexNav/10.gif",
										text:'米粉卡'
									},
								]
							},
							{
								type:"threeeAdv",
								data:{
										big:{
											src:"../../static/images/demo/demo1.jpg"
										},
										smallTop:{
											src:"../../static/images/demo/demo2.jpg"
										},
										smallBottom:{
											src:"../../static/images/demo/demo3.jpg"
										}
									},
							},
							{
								type:"commonList",
								data:[
									{
										cover:"../../static/images/list/1.jpg",
										title:"米家空调",
										desc:"1.5匹变流空调",
										oPrice:"2678",
										nPrice:"1999"
									},
									{
										cover:"../../static/images/list/2.jpg",
										title:"黑鲨手机",
										desc:"游戏性能，散热好",
										oPrice:"2678",
										nPrice:"1299"
									},
									{
										cover:"../../static/images/list/3.jpg",
										title:"红米手机",
										desc:"1.5匹变流空调",
										oPrice:"2678",
										nPrice:"1999"
									},
									{
										cover:"../../static/images/list/4.jpg",
										title:"荣耀",
										desc:"1.5匹变流空调",
										oPrice:"2678",
										nPrice:"1999"
									},
									{
										cover:"../../static/images/list/5.jpg",
										title:"红米redmi",
										desc:"1.5匹变流空调",
										oPrice:"2678",
										nPrice:"1999"
									},
									{
										cover:"../../static/images/list/6.jpg",
										title:"米家平板",
										desc:"本地数据",
										oPrice:"2678",
										nPrice:"1999"
									}
								]
							},]
	let demo2=[{
								type:"swiper",
								data:[
									{
										src:"../../static/images/lc250.png",
									},
									{
										src:"../../static/images/wrangler.png"
									},
									{
										src:"../../static/images/goole.png"
									}
								]
							},
							{
								type:"iconArray",
								data:[
							
									{
										src:"../../static/indexNav/6.gif",
										text:'小米秒杀'
									},
									{
										src:"../../static/indexNav/7.gif",
										text:'真心想要'
									},
									{
										src:"../../static/indexNav/8.gif",
										text:'电视特卖'
									},
									{
										src:"../../static/indexNav/9.gif",
										text:'家电热卖'
									},
									{
										src:"../../static/indexNav/10.gif",
										text:'米粉卡'
									},
								]
							},
							{
								type:"threeeAdv",
								data:{
										big:{
											src:"../../static/images/demo/demo1.jpg"
										},
										smallTop:{
											src:"../../static/images/demo/demo2.jpg"
										},
										smallBottom:{
											src:"../../static/images/demo/demo3.jpg"
										}
									},
							},
							{
								type:"commonList",
								data:[
									{
										cover:"../../static/images/list/1.jpg",
										title:"米家空调",
										desc:"1.5匹变流空调",
										oPrice:"2678",
										nPrice:"1999"
									},
									{
										cover:"../../static/images/list/2.jpg",
										title:"黑鲨手机",
										desc:"游戏性能，散热好",
										oPrice:"2678",
										nPrice:"1299"
									},
									{
										cover:"../../static/images/list/3.jpg",
										title:"红米手机",
										desc:"1.5匹变流空调",
										oPrice:"2678",
										nPrice:"1999"
									}
								]
							},]
	
	import swiperImages from "@/components/index/swiper-images.vue"
	import navIcon from "@/components/index/index-nav.vue"
	import threeAdv from "@/components/index/three-adv.vue"
	import card from "@/components/common/card.vue"
	import commonList from "@/components/common/commList.vue"
	export default {
		components:{
			swiperImages,
			navIcon,
			threeAdv,
			card,
			commonList
		},
		data() {
			return {
				scrollInto:'',
				tabIndex:0,
				scrollH:500,
				tabBars:[],
				newsItems:[],
					
			}
		},
		onLoad() {
		uni.getSystemInfo({
			success: (res) => {
				this.scrollH=res.windowHeight-uni.upx2px(80)
			}
		})
			// 初始化事件
			this.__init()
		},
		methods: {
			// 初始化事件
			__init(){
				// 获取顶部选项卡
				this.tabBars=demoTabars
				// 根据顶部选项卡生成页面
				let arr=[];
				for (let i = 0; i < this.tabBars.length; i++) {
					let obj={
						list:[]
					}
					if (i===0) {
						obj.list=demo1
					}
					arr.push(obj)
				}
				this.newsItems=arr
				console.log(this.newsItems)
			},
			
			
			// 切换选项卡
				changeTab(index){
					if(this.tabIndex===index){
						return;
					}else{
						this.tabIndex=index
						this.scrollInto='tab'+index
						this.addData()
					}
					
				},
				// 监听滑动列表
				onChageTab(e){
					console.log(e.detail.current)
					this.changeTab(e.detail.current)
				},
				addData(){
					let index=this.tabIndex
					this.newsItems[index].list=demo2
				}
				
				
		}
	}
</script>

<style>

</style>