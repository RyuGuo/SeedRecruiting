<template>
	<view>
		<PageHeader :isshowlogo="false"  title="种子班现状"></PageHeader>
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
					"今年6月份毕业的29名16级种子班同学中，就业12人，深造17人。应届毕业生平均年薪高达30.6万元以上，最高薪资达40万元，77.7%的毕业生薪资高于30万，就业去向均为知名互联网公司。深造的毕业生中，12名读硕，5名读博，而他们的去向包括亚洲TOP15名校、国内顶尖人工智能实验室、双一流学科研究所、EMC全美第一Lab等。"
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
