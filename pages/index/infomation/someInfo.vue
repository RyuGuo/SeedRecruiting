<template>
	<div>
		<PageHeader :isshowlogo="false" title="招新相关"></PageHeader>
		<ul class="info-wrap">
			<li v-for="info_item in info" :key="info_item.title">
				<span class="info-title">{{info_item.title}}</span>
				<span class="info-content">{{info_item.content}}</span>
			</li>
		</ul>
		<div class="scan2D">
			<img id="scan2D" :src="scan2DUrl" />
			<p>扫描二维码，加入群聊</p>
		</div>
		<div class="Button-Group">
			<a href="http://recruit.dian.org.cn/register/">
			<div class="Button1">
				<p>现在报名</p>
			</div>
			</a>
			<a href="http://recruit.dian.org.cn/query/">
			<div class="Button2">
				<p>查询进度</p>
			</div>
			</a>
		</div>
	</div>
</template>

<script>
import PageHeader from "../../../components/PageHeader.vue";
export default {
	components: {
		PageHeader,
	},
	data() {
		return {
			// 资料都需要改哦┌(.Д.)┐
			// QQ: '**********',
			scan2DUrl: './static/image/scan2D2.png',
			info: [
				{"title":"报名时间","content":"5月1日~5月9日"},
				{"title":"宣讲时间","content":"5月4日"},
				{"title":"宣讲地点","content":"在线"},
				{"title":"测试开始时间","content":"5月9日"},
				{"title":"测试答辩时间","content":"5月17日"},
				{"title":"","content":""},
				{"title":"团队官网","content":"http://dian.org.cn"},
				// {"title":"报名链接","content":"http://recruit.dian.org.cn"},
				// {"title":"进度查询","content":"http://recruit.dian.org.cn/query"},
			]
		}
	},
	mounted(){
		let dom = document.getElementById("scan2D");
		let Wheight = document.body.clientHeight;
		let Wwidth = document.body.clientWidth;
		console.log(Wheight,Wwidth);
		
		let offsetH = -320;
		let width = Math.min(Wheight+offsetH, 250);
		console.log(width);
		dom.style.width = width + 'px';
		dom.style.height = width + 'px';
	}
}
</script>

<style lang="scss" scoped>
@import "@/style/common.scss";
a{
	text-decoration: none;
}
.info {
	&-wrap {
		margin: 10px 0px 0 80px;
		list-style: none;
		li {
			font-size: 0;
		}
	}
	&-title {
		color: $black;
		font-size: 16px;
		font-weight: bold;
		margin-right: 10px;
	}
	&-content {
		color: $bluegray;
		font-size: 16px;
	}
}
.scan2D {
	margin: 25px 0;
	text-align: center;
	img {
		width: 75px;
		height: 75px;
	}
	p {
		color: $bluegray;
		text-align: center;
		font-size: 12px;
	}
}
.Button-Group {
	position: absolute;
	display: flex;
	justify-content: space-around;
	left: 50%;
	width: 100%;
	bottom: 15px;
	transform: translate(-50%);
}
.Button1 {
	width: 150px;
	height: 44px;
	background: $orange;
	border-radius: 22px;
	display: flex; 
	justify-content: center;
	align-items: center;
	p { 
		text-align: center;
		color: $white;
		font-size: 20px;
	}
}
.Button1:active {
	background: #c37100;
}
.Button2 {
	width: 150px;
	height: 44px;
	background: #fffb8f;
	border-radius: 22px;
	display: flex; 
	justify-content: center;
	align-items: center;
	p { 
		text-align: center;
		color: $orange;
		font-size: 20px;
	}
}
.Button2:active {
	background: #e4e17f;
}
</style>
