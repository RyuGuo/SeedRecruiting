<template>
	<div style="height:100%">
		<PageHeader :isshowlogo="false" title="项目组介绍"></PageHeader>
		<swiper 
			class="swiper" 
			:indicator-dots="true" 
			:autoplay="true" 
			:interval="8000" 
			:duration="1000" 
			current="0" 
			indicator-active-color="rgba(255,255,255,0.8)"
		>
			<block v-for="item in teamInfo" :key="item.name">
				<swiper-item  class="swiper-center">
					<div class="card">
						<TeamCard :name="item.name" 
							:imgUrl="item.imgUrl" 
							:info="item.info"
							:tech="item.tech"
							:abbr="item.abbr"
						></TeamCard>
					</div>
				</swiper-item>
			</block>
		</swiper>
	</div>
</template>

<script>
import PageHeader from "@/components/PageHeader.vue"
import TeamCard from "@/components/TeamCard.vue"
	export default {
		components:{
			PageHeader,
			TeamCard,
		},
		data() {
			return {
				teamInfo: [
					{
						name:"AI组",
						imgUrl: './static/image/AI.png',
						info: 'AI组是团队AI转型的先行军，目前主要研究方向有自然语言处理、计算机视觉、强化学习等。项目组不仅有强大的计算资源，更有一批以王兴刚导师为代表的专业指导老师。沉浸在浓厚的科研氛围中，团队也涌现出了一批研究能力与工程能力兼备的未来AI工程师。目前项目组同时开展有交通废片回滚项目，人脸关键点检测项目等多项前沿研究。',
						tech: '机器学习, 深度学习, 计算机视觉, 自然语言处理, 强化学习',
						abbr: 'AI Group'
					},{
						name:"Intel组",
						imgUrl: './static/image/Intel.png',
						info: 'Intel项目组与世界500强公司Intel合作共同开发5G协议栈，完善Intel商用芯片功能；走在5G学术研究最前沿，进行5G MAC调度算法研究并且Intel组将5G与AI相结合实现实时调度，精准调优。加入Intel组，你可以切身参与到企业级的项目开发流中，学会高效率开发调试；掌握最新的5G协议规范；实现AI算法与5G通信双丰收。而且你还可以获得世界500强公司Intel实习机会。',
						tech: '5G C/C++ Linux AI NS3',
						abbr: 'Intel Group'
					},{
						name:"迅测组",
						imgUrl: './static/image/IoT.png',
						info: '迅测组依托Dian团队老队员们的创业公司，致力于打造电动车行业内首个物联网平台。我们秉承以老带新的优良传统，这里有一批经过多年职场历练的优秀毕业老队员亲身指导，也有众多优秀的学长学姐们传授经验。从硬件到嵌入式、从后台到前端，你可以在自己喜欢的方向大展身手，体验整个项目流程的开发。在这里，你将收获知识、技术、友谊和成长。迅测组欢迎你的加入。',
						tech: '硬件嵌入式，前端，后台',
						abbr: 'Xunce Group'
					},{
						name:"启亦电子组",
						imgUrl: './static/image/qiyi.png',
						info: '启亦电子组是Dian团队的嵌入式组，凡是涉及到硬件的项目都由启亦电子组负责。项目组和上海启亦电子科技有限公司合作开发的电子电力APP，实现了电力测量设备与应用软件交互，目前已经在中国南方电网投入使用。当前正在进行的是和华为合作的镜头防抖测试系统，测试对象是华为最新的旗舰机P30的摄像模组，手握30个全新摄像模组，毫无意外得成为Dian团队最 “壕”项目组！',
						tech: 'SOC软硬件协同开发设计，移动设备Android/IOS应用开发',
						abbr: 'QIYI Electric Group'
					},{
						name:"鹰眼组",
						imgUrl: './static/image/web.png',
						info: '在迭代开发中亲历技术的变革，在页面交互中感受设计的艺术，这是鹰眼组能所给你的。在这里，你可以体验一个项目从立项到交付的整个过程，可以参与企业级的真实项目实践。我们的主要方向为移动互联网开发，包括Web前后端、移动端、微信小程序等的开发，目前正在开发中的项目包括在线考试系统、烟草烘烤系统等。我们期待下一轮的开发因你的参与而更有收获！',
						tech: 'Python，Java，React，Vue，微信小程序等',
						abbr: 'Hawk-Eye Group'
					},{
						name: '网安组',
						imgUrl: './static/image/wangguan.png',
						info: '网安组主要技术特点是网络安全。网安组依托于团队的导师资源和在网络方向深耕多年的技术积累，以及与中科院信工所等资深安全研究机构的合作关系等，致力于研究和应对日益严峻的网络安全形势、培养网络安全方面的人才。在这里，可以深入学习渗透测试、二进制逆向、密码学、机器学习、深度学习等知识，将人工智能与网络安全结合，参与到最前沿的网络安全防护研究中。',
						tech: '渗透测试，二进制逆向，密码学，ML，DL',
						abbr: 'Cyber Security Group'
					},{
						name:"凯卓组",
						imgUrl: './static/image/yueranxindong.png',
						info: '凯卓组和武汉烽火凯卓公司合作开发综合智能管理平台，致力于打造一个面向应用服务的、智能化的、基于网络和高度集中管理的边海防视频监控系统，目标应用场所为广西、黑龙江等边境省的派出所。在这里，不仅可以参与从客户端到服务端的开发、测试和维护，全面提高应用软件工程能力，还能为国家安防贡献一份自己的力量！',
						tech: 'C/C++，PC客户端，服务端，流媒体',
						abbr: 'Pinssible Group'
					},{
						name: '区块链组',
						imgUrl: './static/image/qukuailian.png',
						info: '区块链技术作为比特币的底层技术首次出现在大众的视野中，去中心化的噱头将区块链技术迅速推向了泡沫期的巅峰，过去的一年里，项目贴上区块链的标签，就像是食物覆盖一层食用金箔。而如今，泡沫期已经过去，一项被大众吹捧的“革命技术”脱去浮夸的外衣，究竟内涵有什么？区块链技术的未来如何？加入我们！一起从区块链的最底层，深挖其存在的价值。',
						tech: 'Golang，分布式，p2p，加密',
						abbr: 'Blockchain Group'
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
