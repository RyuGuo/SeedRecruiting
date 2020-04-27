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
					"截至2020年（包括16级种子班，于2020年6月毕业），种子班已毕业学生259名，其中直接工作103人；出国出境（含香港）深造45人；在国内读研111人。学生已累计获得国家级奖项48个，省级奖项41个，企业级奖项19个、校级奖项163个，专利授权数30项，在国内重要期刊以及国际会议发表论文27篇。"
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
.an {
	margin-top: 40px;
	text-align: center;
	font-size: 20px;
	> div {
		font-size: 40px;
	}
}

.starburst {
	display:block;
	width:6em;
	height:6em;
	background:#fe0;
	-webkit-transform:rotate(-45deg);
	-moz-transform:rotate(-45deg);
	rotation:-45deg;
	position:relative;
	top:2em;
	left:2em;
	text-align:center;
	text-decoration:none;
	color:#000;
	font-weight:bold;
	font-family:Arial, sans-serif;
}
.starburst span {
	display:block;
	width:6em;
	height:6em;
	background:#fe0;
	-webkit-transform:rotate(22.5deg);
	-moz-transform:rotate(22.5deg);
	rotation:22.5deg;
}
</style>
