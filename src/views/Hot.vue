<template>
	<div class="CardHot HotList">
		
		
		
		
		<!-- 顶部tab导航 -->
		<ul class="tab-title border-bottom">
			<li v-for="(title, index) in tabTitle" @click="change(index)" 
			:class="{ active: cur == index }" :key="index">
			{{ title }}
		   </li>
		</ul>
		<!-- 切换的内容区 -->
		<div>
			
			
			<div v-for="(content, index) in tabContent" v-show="cur == index" :key="index">
				<section tabindex="0" class="HotItem" v-for="(item, index1) in content" :key="index1" >
					<div class="HotItem-index">
						<div class="HotItem-rank"><h3 class="light-grey" :class="{ top: index1 < 3 }">{{ index1 + 1 }}</h3></div>
					</div>
					<div class="HotItem-content"><a :href="'https://www.zhihu.com/question/' + item.target.id" target="_blank" class="sub-title">
							<h2 class="HotItem-title">{{ item.target.title }}</h2>
							<p class="HotItem-excerpt">{{ item.target.excerpt }}</p>
						</a>
						<div class="HotItem-metrics HotItem-metrics--bottom">
							<svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--Hot"
							 fill="currentColor" viewBox="0 0 24 24" width="18" height="18">
								<path fill="url(#id-2014200654-a)" fill-rule="evenodd" d="M 14.553 20.78 c 0.862 -0.651 1.39 -1.792 1.583 -3.421
								 c 0.298 -2.511 -0.656 -4.904 -2.863 -7.179 c 0.209 2.291 0.209 3.73 0 4.314 c -0.41 1.143 -1.123 1.983 -1.91 2.03 
								 c -1.35 0.079 -2.305 -0.512 -2.863 -1.774 c -0.676 1.25 -0.782 2.556 -0.318 3.915 c 0.31 0.906 0.94 1.684 1.89 2.333
								  C 7.144 20.131 5 17.336 5 14.022 c 0 -2.144 0.898 -4.072 2.325 -5.4 c 0.062 2.072 0.682 3.598 2.13 4.822 c -0.67 -1.112
								   -0.734 -2.11 -0.734 -3.517 c 0 -3.253 2.067 -6.007 4.913 -6.927 a 7.35 7.35 0 0 0 2.157 4.918 C 17.722 9.214 19 11.463
									19 14.022 c 0 3.073 -1.844 5.7 -4.447 6.758 Z" />
							</svg>{{ item.detail_text }}
							
							<span class="HotItem-action">
								<div class="Popover ShareMenu">
									<div class="ShareMenu-toggler" id="Popover110-toggle" aria-expanded="false" aria-haspopup="true" aria-owns="Popover110-content"><button
										 class="Button Button--plain Button--withIcon Button--withLabel" type="button"><span style="display: inline-flex; align-items: center;">​<svg
												 xmlns="http://www.w3.org/2000/svg" class="Zi Zi--Share Button-zi" fill="currentColor" viewBox="0 0 24 24"
												 width="1.2em" height="1.2em">
													<path fill-rule="evenodd" d="M 2.931 7.89 c -1.067 0.24 -1.275 1.669 -0.318 2.207 l 5.277 2.908 l 8.168 -4.776 c 0.25 -0.127 0.477 0.198 0.273 0.39 L 9.05 14.66 l 0.927 5.953 c 0.18 1.084 1.593 1.376 2.182 0.456 l 9.644 -15.242 c 0.584 -0.892 -0.212 -2.029 -1.234 -1.796 L 2.93 7.89 Z" /></svg></span>分享</button></div>
								</div>
							</span></div>
					</div>
					<a class="HotItem-img" v-if="item.children[0].thumbnail">
					 <img :src="item.children[0].thumbnail" width="180px" height="105px" class="tiny-round mt-3" /></a>
				</section>
				
				
				
				
				
			
				<p class="tx-center light-grey mt-4 mb-4 no-more">没有更多内容</p>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'hot',
	data() {
		return {
			tabTitle: ['全站', '科学', '数码', '体育', '时尚', '影视', '校园', '汽车'],
			category: ['total', 'science', 'digital', 'sport', 'fashion', 'film', 'school', 'car'],
			tabContent: [[], [], [], [], [], [], [], []],
			cur: 0
		};
	},
	created() {
		this.axios.get('/api/hot-lists/total').then(res => {
			this.tabContent.splice(0, 0, res.data.data.data);
		});
	},
	methods: {
		change(index) {
			this.cur = index;
			//取出对应的参数数组的值
			let param = this.category[index];
			//发起对应请求
			this.axios.get('/api/hot-lists/' + param).then(res => {
				this.tabContent.splice(index, 0, res.data.data.data);
			});
			if (param == 'total') {
				this.$router.push('/home/hot');
			} else {
				this.$router.push('/home/hot?list=' + param);
			}
			
		}
	}
};
</script>
<style lang="scss" scoped>
	
	.HotList {
	    position: relative;
	    background: #fff;
	    border-bottom-left-radius: 2px;
	    border-bottom-right-radius: 2px;
	    -webkit-box-sizing: border-box;
	    box-sizing: border-box;
	    -webkit-box-shadow: 0 1px 3px 0 rgba(0,34,77,.05);
	    box-shadow: 0px 1px 3px 0px rgba(0,34,77,0.05);
	}

.tab-title {
	display: flex;
	align-items: center;
	height: 63px;
	padding: 0.625rem;
	background-color: #fff;
	li {
		width: 68px;
		height: 30px;
		line-height: 30px;
		text-align: center;
		border-radius: 2px;
		margin: 8px;
		background-color: #f6f6f6;
		color: #646464;
		cursor: pointer;
	}
	.active {
		background-color: #e6f3ff;
		color: #0c89ff;
	}
}
.top {
	color: #fc9300;
}
.no-more:before,
.no-more:after {
	content: '';
	display: inline-block;
	width: 24px;
	height: 1px;
	margin: 0 10px;
	vertical-align: middle;
	background-color: #d3d3d3;
}
.mt-2 {
	cursor: pointer;
	&:hover {
		color: #646464;
	}
}


.HotItem {
	    background: #fff;
	    display: -webkit-box;
	    display: -ms-flexbox;
	    display: flex;
	    padding: 16px 16px 40px 0;
	    position: relative;
	}
:not(:first-child).HotItem {
    border: solid #ebebeb;
    border-width: .5px 0 0;
}
.HotItem-index {
    text-align: center;
    width: 57px;
}
.HotItem-rank {
    line-height: 1.6;
    font-size: 18px;
    color: #999;
    font-weight: 600;
    font-synthesis: style;
}
.HotItem-content {
    -webkit-box-flex: 1;
    -ms-flex: 1 1;
    flex: 1 1;
    overflow: hidden;
}
.HotItem-title {
    color: #1a1a1a;
    font-size: 18px;
    line-height: 28px;
    max-height: 56px;
    display: -webkit-box;
    text-overflow: ellipsis;
    overflow: hidden;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    font-weight: 600;
    font-synthesis: style;
}
.HotItem-excerpt {
    color: #444;
    line-height: 25px;
    margin-top: 2px;
    min-height: 25px;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}
.HotItem-metrics--bottom {
    bottom: 16px;
    position: absolute;
}
.HotItem-metrics {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    color: #8590a6;
    font-size: 14px;
    height: 16px;
    margin-top: 8px;
}
.HotItem-metrics {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    color: #8590a6;
    font-size: 14px;
    height: 16px;
    margin-top: 8px;
}
.HotItem-metrics path {
    fill: #9fadc7;
}.HotItem-metrics .HotItem-action {
    margin-left: 28px;
}
.Popover {
    position: relative;
    display: inline-block;
}
.HotItem-img::after, .HotItem-img img {
    border-radius: 4px;
    height: 105px;
    width: 190px;
}
.HotItem-img {
    display: block;
    height: 105px;
    margin-left: 16px;
    position: relative;
}
.tx-center {
  
       left: 0px;
       right: 0px;
       top: 100%;
       padding: 30px 0;
       text-align: center;
       color: #999;
  
}
</style>