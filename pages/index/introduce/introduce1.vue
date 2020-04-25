<template>
	<div>
		<PageHeader :isshowlogo="false"  title="种子班介绍"></PageHeader>
		<div class="text">
			<TextContent 
				:contentList="contentList"
			></TextContent>
		</div>
	</div>
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
				contentList:[
					'“种子班”，全称基于项目的信息类专业教育实验班。2006年，分管本科教学的校领导建议设立“种子班”，把Dian团队的“干中学”模式纳入到体制内。种子班依托电信学院的电子信息工程专业进行专业培养，纳入启明学院实验班管理规范。目前，种子班已招生14届，每届1个自然班30人，从大三开始独立建班。',
					'种子班实行导师制、导生制和顾问制。导师为每名学生制定个性化的培养方案，实施科研项目牵引下的研究性和实践性教学。本科阶段，种子班学生通常会进行2个真实科研项目的训练，从跟项目、做项目到管项目，以递进方式得到提升，为未来成为行业领军人才打牢基础。'
				]
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
@import "@/style/text.scss";
@import "@/style/common.scss";
.text {
	margin-top: 20px;
}
</style>
