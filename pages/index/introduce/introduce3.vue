<template>
	<view>
		<PageHeader :isshowlogo="false"  title="Dian团队介绍"></PageHeader>
		<div class="text">
		<TextContent
			:contentList="contentList"
		></TextContent>
		</div>
	</view>
</template>

<script>
import PageHeader from "@/components/PageHeader.vue"
import TextContent from "@/components/TextContent.vue"
	
	export default {
		components: {
			PageHeader,
			TextContent,
		},
		data() {
			return {
				contentList: [
					"Dian团队全称是“基于导师制的本科人才孵化站”，由刘玉教授于2002年3月创建，并成为首批入驻启明学院的学生团队。通过“干中学”的培养模式，辅以真实项目的切身实践，培养学生的创新能力、实践精神和综合素质，是团队的初衷。",
					"“历平凡事，成放心人”，是团队的口号。Dian团队经过18年的成长，在导师和历届队员的共同奋斗下，逐渐发展壮大，团队有28名顾问，均是各个行业的专家学者、领军人物。17年来已经走出了50多家创业公司，其中两家独角兽，十余家估值过亿，有四名队员入选福布斯“中国30位30岁以下创业者”榜单，因为其优异的育人成果受到了包括人民日报、科技日报在内的多家媒体报道及省部级和国家领导人的多次接见。"
				]
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
@import "@/style/text.scss";
.text {
	margin-top: 20px;
}
</style>
