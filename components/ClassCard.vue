<template>
	<div class="wrap">
		<div class="name">{{name}}</div>
		<div class="info">{{info}}</div>
		<img class="img" :src="imgUrl" mode="aspectFit"></img>
		<div class="imgTitle">{{imgTitle}}</div>
	</div>
</template>

<script>
	export default {
		props: {
			imgUrl: String,
			name: String,
			info: String,
			imgTitle: String
		},
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
.wrap {
	width: 260px;
	background: rgba(255,255,255,0.85);
	border: 1px $gray solid;
	border-radius: 8px;
	box-shadow: 3px 4px 6px rgba(0,0,0,0.3);
	padding: 10px 20px;
}

.img {
	margin-top: 40px;
	width: 100%;
}

.name {
	margin-top: 20px;
	font-size: 20px;
	font-weight: bold;
}

.info {
	font-size: 16px;
	margin-top: 10px;
	text-indent: 2em;
}

.imgTitle {
	font-size: 14px;
	text-align: center;
}
</style>
