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
					'种子班是Dian团队的“黄埔军校”，加入种子班的同学同时自动加入Dian团队，并且需要参与到Dian团队的项目实践与日常事务管理中来。参与团队与企业合作的项目是种子班同学的必修课，每学期有5到10个不等的工程训练的学分，在“跟项目”、“做项目”、“管项目”过程中，学生的技术能力和管理能力都得到很大提升。项目之余，种子班的同学们还要参与到团队日常的管理中来，例如接待外界的参观、举办一年一度的种子杯大赛等。对于种子班的同学来说，无论是项目经历，还是团队服务经历，对他们而言都是一个很好的历练。'
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
