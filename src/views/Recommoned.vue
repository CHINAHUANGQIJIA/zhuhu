<template>
		<div>
		<div v-for="(item, index) in recommenedList" :key="index" class="Card maincard maincard-isRecommend" >
			<div class="Recommendtext "  >
				<h2 class="Recommendtext-title" >
						<a v-if="item.target.question == null" >{{item.target.title}}
						</a>
						<h3 v-else >{{ item.target.question.title }}
						</h3>
					
				</h2>
				
				<div class="miantext is-collapsed" v-if="!flags[index]" >
					<div class="miantext-cover" v-if="item.target.thumbnail"  >
						<div class="miantext-cover-inner" ><img :src="item.target.thumbnail">
						</div>
							</div>
						<div class="miantext-inner">
						<span class="RichText ztext CopyrightRichText-richText" itemprop="text">
							 {{ item.target.author.name }}:{{ item.target.excerpt.substring(0,70)}}
						
						
						
							<span class="read-more link" @click="change(index)">
								<span class="Button Recommendtext-more Button--plain" type="button" style="color: #175199;" >阅读全文
								
								<span style="display: inline-flex; align-items: center;">
								 ​<svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--ArrowDown Recommendtext-arrowIcon" fill="currentColor" viewBox="0 0 24 24" width="24" height="24">
								<path fill-rule="evenodd" d="M 12 13 L 8.285 9.218 a 0.758 
								0.758 0 0 0 -1.064 0 a 0.738 0.738 0 0 0 0 1.052 
								l 4.249 4.512 a 0.758 0.758 0 0 0 1.064 0 l 4.246 
								-4.512 a 0.738 0.738 0 0 0 0 -1.052 a 0.757 0.757 
								0 0 0 -1.063 0 L 12.002 13 Z" /></svg>
								</span>
								</span>
								     </span>
							</span>
						</div>
					
				</div>
				<!-- 点击“阅读全文”显示 -->
				<div v-if="flags[index]" class="p-2">
					<div class="d-inline-flex">
						<img :src="item.target.author.avatar_url" class="avatar mr-2" />
						<h4 class="mr-2">{{ item.target.author.name }}</h4>
						<span>{{ item.target.author.headline }}</span>
					</div>
					
					<p class="light-grey mt-2 mb-2">{{ item.target.voteup_count }}人赞同了该回答</p>
					<div v-html="item.target.content" class="content"></div>
				</div>
			</div>

			<ul class="Recommendtext-actions" :class="{ active: flags[index] }">
			<button class="Button VoteButton VoteButton--up" aria-label="赞同 8K" type="button">
					<svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--TriangleUp VoteButton-TriangleUp" fill="currentColor" viewBox="0 0 24 24" width="10" height="10"><path fill-rule="evenodd" d="M 2 18.242 c 0 -0.326 0.088 -0.532 0.237 -0.896 l 7.98 -13.203 C 10.572 3.57 11.086 3 12 3 c 0.915 0 1.429 0.571 1.784 1.143 l 7.98 13.203 c 0.15 0.364 0.236 0.57 0.236 0.896 c 0 1.386 -0.875 1.9 -1.955 1.9 H 3.955 c -1.08 0 -1.955 -0.517 -1.955 -1.9 Z" /></svg>
					赞同{{ item.target.voteup_count }}
				</button>
				
			<button class="Button VoteButton VoteButton--down" aria-label="反对" type="button">
										<span style="display: inline-flex; align-items: center;">​
			<svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--TriangleDown" fill="currentColor" viewBox="0 0 24 24" width="10" height="10">
										<path fill-rule="evenodd" d="M 20.044 3 H 3.956 C 2.876 3 
										2 3.517 2 4.9 c 0 0.326 0.087 0.533 0.236 0.896 L 10.216 
										19 c 0.355 0.571 0.87 1.143 1.784 1.143 s 1.429 -0.572 1.784
										 -1.143 l 7.98 -13.204 c 0.149 -0.363 0.236 -0.57 0.236 -0.896 
										 c 0 -1.386 -0.876 -1.9 -1.956 -1.9 Z" /></svg></span>
										 </button>
										 
										 
										 </span>
										 <button class="Button Recommendtext-action Button--plain Button--withIcon Button--withLabel" type="button">
										 							<span style="display: inline-flex; align-items: center;">​
										 <svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--Comment Button-zi" fill="currentColor" viewBox="0 0 24 24" width="1.2em" height="1.2em">
										 					        <path fill-rule="evenodd" d="M 10.241 19.313 a 0.97 0.97 0
										 							 0 0 -0.77 0.2 a 7.908 7.908 0 0 1 -3.772 1.482 a 0.409 0.409
										 							  0 0 1 -0.38 -0.637 a 5.825 5.825 0 0 0 1.11 -2.237 a 0.605
										 							   0.605 0 0 0 -0.227 -0.59 A 7.935 7.935 0 0 1 3 11.25 C 3
										 								6.7 7.03 3 12 3 s 9 3.7 9 8.25 s -4.373 9.108 -10.759
										 								 8.063 Z" /></svg></span>{{ item.target.comment_count }}条评论</button>

		
				<li class="Button Recommendtext-action Button--plain Button--withIcon Button--withLabel">
					<span style="display: inline-flex; align-items: center;">​
					<svg class="Zi Zi--Comment Button-zi" fill="currentColor" viewBox="0 0 24 24" width="1.2em" height="1.2em">
						<path
							d="M2.931 7.89c-1.067.24-1.275 1.669-.318 2.207l5.277 2.908 8.168-4.776c.25-.127.477.198.273.39L9.05 14.66l.927 5.953c.18 1.084 1.593 1.376 2.182.456l9.644-15.242c.584-.892-.212-2.029-1.234-1.796L2.93 7.89z"
							fill-rule="evenodd"
						></path>
					</svg></span>
					分享
				</li>
				<li class="Button Recommendtext-action Button--plain Button--withIcon Button--withLabel">
					<span style="display: inline-flex; align-items: center;">​
					<svg class="Zi Zi--Comment Button-zi" fill="currentColor" viewBox="0 0 24 24" width="1.2em" height="1.2em">
						<path
							d="M5.515 19.64l.918-5.355-3.89-3.792c-.926-.902-.639-1.784.64-1.97L8.56 7.74l2.404-4.871c.572-1.16 1.5-1.16 2.072 0L15.44 7.74l5.377.782c1.28.186 1.566 1.068.64 1.97l-3.89 3.793.918 5.354c.219 1.274-.532 1.82-1.676 1.218L12 18.33l-4.808 2.528c-1.145.602-1.896.056-1.677-1.218z"
							fill-rule="evenodd"
						></path>
					</svg></span>
					收藏
				</li>
				<li class="Button Recommendtext-action Button--plain Button--withIcon Button--withLabel">
					<span style="display: inline-flex; align-items: center;">​
					<svg class="Zi Zi--Comment Button-zi" fill="currentColor" viewBox="0 0 24 24" width="1.2em" height="1.2em">
						<path
							d="M2 8.437C2 5.505 4.294 3.094 7.207 3 9.243 3 11.092 4.19 12 6c.823-1.758 2.649-3 4.651-3C19.545 3 22 5.507 22 8.432 22 16.24 13.842 21 12 21 10.158 21 2 16.24 2 8.437z"
							fill-rule="evenodd"
						></path>
					</svg></span>
					喜欢
				</li>
				<li class="Button Recommendtext-action Button--plain Button--withIcon Button--withLabel">
					<span style="display: inline-flex; align-items: center;">​
					<svg class="Zi Zi--Comment Button-zi" fill="currentColor" viewBox="0 0 24 24" width="1.2em" height="1.2em">
						<path d="M5 14a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm7 0a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm7 0a2 2 0 1 1 0-4 2 2 0 0 1 0 4z" fill-rule="evenodd"></path>
					</svg></span>
				</li>
				
				
				<button  class="Button Recommendtext-action Recommendtext-rightButton Button--plain" @click="change(index)" v-if="flags[index]">
					<span class="miantext-collapsedText">收起</span>
				<span style="display: inline-flex; align-items: center;">​
				<svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--ArrowDown Recommendtext-arrowIcon is-active" fill="currentColor" viewBox="0 0 24 24" width="24" height="24"><path fill-rule="evenodd" d="M 12 13 L 8.285 9.218 a 0.758 0.758 0 0 0 -1.064 0 a 0.738 0.738 0 0 0 0 1.052 l 4.249 4.512 a 0.758 0.758 0 0 0
				 1.064 0 l 4.246 -4.512 a 0.738 0.738 0 0 0 0 -1.052 a 0.757 0.757 0 0 0 -1.063 0 L 12.002 13 Z" /></svg>
					</span></button>
				
			</ul>
		</div>
	</div>
</template>


<script>
export default {
	name: 'recommoned',
	data() {
		return {
			recommenedList: [],
			flags: []
		};
	},
	mounted() {
		window.addEventListener('scroll', this.scrollToTop);
	},
	created() {
		this.axios.get('/api/recommend').then(res => {
			this.recommenedList = res.data.data.data;
			//定义一个正则规则，用来处理富文本中的图片
			const regex = new RegExp('<img', 'gi');
			for (var i = 0; i < this.recommenedList.length; i++) {
				//给每篇文章添加一个标记，默认为false，表示未展开全文
				this.flags.splice(i, 0, false);
				//将富文本中的图片处理大小
				this.recommenedList[i].target.content = this.recommenedList[i].target.content.replace(regex, `<img style="max-width: 100%; height: auto"`);
			}
		});
	},
	methods: {
		//展开、收起的切换
		change(index) {
			//将flag数组索引为index的项置反，注意splice用法，不要直接给数组元素赋值（无法监听flag变化）
			this.flags.splice(index, 1, !this.flags[index]);
		}
	}
};
</script>

<style>
	
.maincard {
		border-radius: 0;
		overflow: visible;
		overflow: initial;
		position: relative;
		padding: 16px 20px;
	}
	
	.Card {
		
		
		border-bottom: 1px solid #f6f6f6;
		background: #fff;
		overflow: hidden;
		border-radius: 2px;
		-webkit-box-shadow: 0 1px 3px rgba(26, 26, 26, .1);
		box-shadow: 0px 1px 3px rgba(26, 26, 26, 0.1);
		-webkit-box-sizing: border-box;
		box-sizing: border-box;
	}


	a {
		color: #1a1a1a;
	}
	
	.Recommendtext-title {
		
		color: #1a1a1a;
		font-size: 18px;
		font-weight: 600;
		font-synthesis: style;
		line-height: 1.6;
	

		margin-bottom: -4px;
	
	}
	
	/*@media all and (min-width:690px)*/
	.miantext.is-collapsed {
		cursor: pointer;
		-webkit-transition: color .14s ease-out;
		transition: color .14s ease-out;
	}
	
	.miantext {
		line-height: 1.67;
	}
	
	.miantext-cover {
		position: relative;
		width: 190px;
		height: 105px;
		margin-top: -2px;
		margin-right: 18px;
		margin-bottom: 4px;
		float: left;
		overflow: hidden;
		background-position: 50%;
		background-size: cover;
		border-radius: 4px;
		-webkit-transform: translateZ(0px);
		transform: translateZ(0px);
	}
	
	.miantext-cover-inner {
		position: absolute;
		top: 50%;
		left: 0px;
		height: 100%;
		width: 100%;
		-webkit-transform: translateY(-50%);
		transform: translateY(-50%);
		overflow: hidden;
	}
	
	.miantext-cover-inner img {
		position: absolute;
		top: 50%;
		left: 50%;
		width: 100%;
		-webkit-transform: translate3d(-50%, -50%, 0px);
		transform: translate3d(-50%, -50%, 0px);
	}
	
	.miantext-cover-play {
		position: absolute;
		z-index: 2;
		left: 0px;
		right: 0px;
		top: 0px;
		bottom: 0px;
		margin: auto;
		width: 48px;
		height: 48px;
		-webkit-box-shadow: 0 0 4px 0 rgba(26, 26, 26, .16);
		box-shadow: 0px 0px 4px 0px rgba(26, 26, 26, 0.16);
		border-radius: 50%;
	}
	
	/*@media all and (min-width:690px)*/
	.miantext.is-collapsed {
		cursor: pointer;
		-webkit-transition: color .14s ease-out;
		transition: color .14s ease-out;
	}
	
	
	.miantext-cover+.miantext-inner {
		margin-top: 16px;
	}
	
	.miantext-inner {
		margin-top: 9px;
		margin-bottom: -4px;
		overflow: hidden;
	}
	
	:not(.miantext--unescapable).miantext.is-collapsed .CopyrightRichText-richText {
		white-space: normal;
	}
	
	.ztext {
		    
		        overflow: hidden;
		        text-overflow: ellipsis;
		        display: -webkit-box;
		        
		        -webkit-box-orient: vertical;
	
	}
	
	.Recommendtext-more {
		padding: 0;
		margin-left: 4px;
		
		
	}
	
	.Button--link,
	.Button--plain {
		height: auto;
		padding: 0;
		color: #76839b;
		line-height: inherit;
		background-color: transparent;
		border: none;
		border-radius: 0;
		
	}
	
	.Button {
		display: inline-block;
		padding: 0 16px;
		font-size: 14px;
		line-height: 32px;
		text-align: center;
		cursor: pointer;
		background: none;
		border: 1px solid;
		border-radius: 3px;
	}
	
	.Recommendtext-actions {
		display: -webkit-box;
		display: -ms-flexbox;
		display: flex;
		-webkit-box-align: center;
		-ms-flex-align: center;
		align-items: center;
		padding: 10px 20px;
		margin: 0 -20px -10px;
		color: #646464;
		background: #fff;
		clear: both;
			
		    
		

	}
	
	.maincard :not(.Button--plain):not(.Button--link).Button {
		line-height: 30px;
		padding: 0 12px;
	}
	
	.VoteButton {
		padding: 0 10px;
		color: #0084ff;
		background: rgba(0, 132, 255, .1);
		border-color: transparent;
	}

	
	.VoteButton--down {
		margin-left: 4px;
	}
	
	.Button--withIcon.Button--link,
	.Button--withIcon.Button--plain {
		padding: 0;
	}
	
	.Recommendtext-action {
		margin-left: 24px;
		font-size: 14px;
	}
	
	.Recommendtext-actions>* {
		-ms-flex-negative: 0;
		flex-shrink: 0;
	}
	


	.read-more {
		position: relative;
		.deep-blue-icon {
			position: absolute;
			bottom: -2px;
		}
	}
	.Button--withIcon.Button--withLabel .Button-zi {
		margin-right: 4px;
	}
	.Recommendtext-rightButton {
	    margin-left: auto;
	}

</style>
