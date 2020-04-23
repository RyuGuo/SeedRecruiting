<template>
	<div style="height:100%">
		<PageHeader :isshowlogo="false" title="特色课程介绍"></PageHeader>
		<swiper 
			class="swiper" 
			:indicator-dots="true" 
			:autoplay="false" 
			:interval="8000" 
			:duration="2000" 
			current="0" 
			indicator-active-color="rgba(255,255,255,0.8)"
		>
			<block v-for="item in classInfo" :key="item.name">
				<swiper-item class="swiper-center">
					<div class="card">
						<ClassCard
							:imgUrl="item.imgUrl"
							:name="item.name"
							:info="item.info"
							:imgTitle="item.imgTitle"
						></ClassCard>
					</div>
				</swiper-item>
			</block>
		</swiper>
	</div>
</template>

<script>
import PageHeader from "@/components/PageHeader.vue"
import ClassCard from "@/components/ClassCard.vue"
	export default {
		components:{
			PageHeader,
			ClassCard,
		},
		data() {
			return {
				classInfo: [
					{
						name:"微机原理与嵌入式系统设计",
						imgUrl: './static/image/class/weiji.png',
						info: '它用与众不同的教学方式引导同学们独立思考、动手实践，让同学们从一块单片机中领略到系统设计的精髓',
						imgTitle: '15级种子班同学在讨论问题'
					},
					{
						name: 'SoC软硬件协同设计',
						imgUrl: './static/image/class/soc.png',
						info: '由美国罗斯豪曼理工学院宋建建教授开设,带领同学们步步为营动手实验，让大家领略软硬件协同设计的魅力',
						imgTitle: '宋老师在给15级种子班上课'
					},
					{
						name: '批判性思维',
						imgUrl: './static/image/class/pipan.png',
						info: '由加拿大董毓博士主讲,倡导积极互动、深度交流，为思辨赋能',
						imgTitle: '15级种子班与董毓老师合影'
					},
					{
						name: '商业企业管理',
						imgUrl: './static/image/class/qiye.png',
						info: '由来自企业界的唐德华顾问讲授,真实案例通人性，实地考察晓管理',
						imgTitle: '唐顾问带15级种子班参观华工科技'
					}
				]
			}
		},
		methods:{
			
		}
	}
</script>

<style lang="scss">
.card {
	display: flex;
	justify-content: center;
	width: 100%;
}
</style>
