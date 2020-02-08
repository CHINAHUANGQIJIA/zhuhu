<template>
	<div>
		<div class="container">
			<div class="row">
				<div class="banner">
							<i class="iconfont"><svg class="Zi Zi--Star" fill="currentColor" viewBox="0 0 24 24" width="36" height="36"><path d="M5.515 19.64l.918-5.355-3.89-3.792c-.926-.902-.639-1.784.64-1.97L8.56 7.74l2.404-4.871c.572-1.16 1.5-1.16 2.072 0L15.44 7.74l5.377.782c1.28.186 1.566 1.068.64 1.97l-3.89 3.793.918 5.354c.219 1.274-.532 1.82-1.676 1.218L12 18.33l-4.808 2.528c-1.145.602-1.896.056-1.677-1.218z" fill-rule="evenodd"></path></svg></i>
					<h3>热门收藏夹</h3>
				</div>
				<div class="" v-for="(item,index)  in favorite" v-if="index>begin&&index<end" :key="index">
	<div class="fcollectionCard">
		<div class="fleftArea">
			<a  class="ftitle" >{{item.title}}</a>
			<div class="fusernameCard">
				<span class="fuserimage">
			
					<a class="UserLink-link" >
						<img  width="28" height="28" :src="item.creatorAvatar" alt="Will"></a>
						
						</span>
						<span class="ftexttitle">{{item.creatorName}}</span>
						<span class="chuangjian">创建</span>
						</div>
						<div class="followers">
							<button class="ffollowButton">关注收藏夹</button>
							<span class="ffollowersCount">{{item.followers}} 人关注</span>
							</div>
							</div>
							<div class="frightCard">
								
									
										<a class="fquestionTitle" >{{item.questionTitle}}</a>
						<div class="fquestiontext">{{item.answerAuthorName}}:{{item.answerContent}}</div>
						<div class="fanswercard">
							<span class="fanswer">回答</span>
							<span class="fcomment">{{item.voteupCount}} 赞同</span>
							<span class="fcomment">{{item.commentCount}} 评论</span>
							</div>
						
							
							<a href="/collection/20158534" class="fCollection"  >已收藏 {{item.totalCount}} 条内容<svg class="Zi Zi--ArrowRight" fill="currentColor" viewBox="0 0 24 24" width="24" height="24">
							<path d="M9.218 16.78a.737.737 0 0 0 
							1.052 0l4.512-4.249a.758.758 0 0 0 0-1.063L10.27 7.22a
							.737.737 0 0 0-1.052 0 .759.759 0 0 0-.001 1.063L13 12l-3.782 3.
							716a.758.758 0 0 0 0 1.063z" fill-rule="evenodd">
							</path>
							</svg>
							</a>
							</div>
							</div>
			</div>
			</div>
			<button @click="show_all" class="flex center l">展开全部>>></button>
		</div>
		<div><a href="#top" style="position: fixed; bottom: 5%; right: 5%;"><i class="iconfont">&#xe633;</i></a></div>
	</div>
</template>

<script>
export default{
	name:'special',
	data(){
		return{
			favorite:[],
			begin:0,
			end:6,
		};
	},
	created() {
		this.axios.get('http://localhost:8080/api/favorite/all').then(res =>{
			console.log(res);
			this.favorite = res.data.data;
		});
	},
	methods: {
	show_all(){
	this.begin=0;
	this.end =this.favorite.length;
	}						
	},					
};
</script>

<style  lang="scss" scoped>
	/*收藏夹内容布局*/
	.fcollectionCard {
	    display: -webkit-box;
	    display: -ms-flexbox;
	    display: flex;
		margin-bottom:10px;
	    padding: 24px;
	    width: 1000px;
	    height: 179px;
	    -webkit-box-sizing: border-box;
	    box-sizing: border-box;
	    background-color: #fff;
	    -webkit-box-shadow: 0 1px 3px 0 rgba(26,26,26,.1);
	    box-shadow: 0 1px 3px 0 rgba(26,26,26,.1);
	}
	
	/*左边*/
	.fleftArea {
	    width: 270px;
	    height: 131px;
	}
	/*标题*/
	.ftitle {
	    display: block;
	    height: 24px;
	    line-height: 24px;
	    font-size: 16px;
	    white-space: nowrap;
	    overflow: hidden;
	    text-overflow: ellipsis;
	    font-weight: 600;
	    font-synthesis: style;
	}
	/*头像和创建人一栏的大小布局*/
	.fusernameCard {
	    display: -webkit-box;
	    display: -ms-flexbox;
	    display: flex;
	    -webkit-box-align: center;
	    -ms-flex-align: center;
	    align-items: center;
	    margin-top: 16px;
	    height: 28px;
	
	}
	/*创建*/
	.chuangjian {
		flex-shrink: 0;
		    margin-left: 4px;
	    line-height: 21px;
	    font-size: 14px;
	    color: #999;
	}
	
	/*创建人头像*/
	.fuserimage {
	    height: 28px;
	    line-height: 28px;
		width: 28px;
		height: 28px;
		
	}
	
	/*收藏块标题*/
	.ftexttitle {
	    cursor: pointer;
	    margin-left: 8px;
	    color: #444;
	    font-weight: 500;
	    white-space: nowrap;
	    overflow: hidden;
	    text-overflow: ellipsis;
	}
	/*更多收藏按钮*/
	.duo{
		font-size: 15px;
		display: flex;
		align-items: center;
		padding: 0 14px 0 24px;
		height: 48px;
		width: 140px;
		background-color: #fff;
		border-radius: 25px;
		color: #778087;
		cursor: pointer;
		font-weight: 600;
		
	}/*关注收藏夹按钮与关注人数模块*/
	.followers {
	    margin-top: 29px;
	}
	/*关注收藏按钮*/
	/*关注收藏夹按钮*/
	.ffollowButton{
		padding: 0;
		font: inherit;
		color: inherit;
		cursor: pointer;
		background: none;
		border: none;
		outline: none;
		-webkit-appearance: none;
		-moz-appearance: none;
		appearance: none;
	    -ms-flex-negative: 0;
	    flex-shrink: 0;
	    width: 102px;
	    height: 34px;
	    background-color: rgba(0,132,255,.08);
	    font-size: 14px;
	    color: #0084ff;
	    border-radius: 3px;
	    font-weight: 600;
	    font-synthesis: style;
	}
	/*关注人数*/
	.ffollowersCount {
	    margin-left: 16px;
	    color: #999;
	    font-size: 14px;
	}
	/*右边*/
	.frightCard {
	    -webkit-box-flex: 1;
	    -ms-flex: 1 1;
	    flex: 1 1;
	    margin-left: 20px;
	    padding-left: 20px;
	    height: 131px;
	    border-left: 1px solid #ebebeb;
	    overflow: hidden;
	}
	/*置顶问题标题*/
	.fquestionTitle {
	    display: block;
	    height: 21px;
	    line-height: 21px;
	    white-space: nowrap;
	    overflow: hidden;
	    text-overflow: ellipsis;
	    font-weight: 600;
	    font-synthesis: style;
		
		
	}
	/*置顶问题内容*/
	.fquestiontext {
	    margin-top: 4px;
	    max-height: 42px;
	    line-height: 21px;
	    color: #444;
	    display: -webkit-box;
	    text-overflow: ellipsis;
	    overflow: hidden;
	    -webkit-line-clamp: 2;
	    -webkit-box-orient: vertical;
	}
	/*回答模块*/
	.fanswercard {
	    display: -webkit-box;
	    display: -ms-flexbox;
	    display: flex;
	    -webkit-box-align: center;
	    -ms-flex-align: center;
	    align-items: center;
	    margin-top: 8px;
	}
	/*回答*/
	.fanswer {
	    height: 17px;
	    line-height: 17px;
	    font-size: 12px;
	    color: #999;
	}
	/*赞同评论*/
	.fcomment {
	    height: 20px;
	    line-height: 20px;
	    padding: 0 4px;
	    background-color: #f6f6f6;
	    color: #999;
	    font-size: 12px;
	    margin-right: 8px;
	    border-radius: 2px;
	}
	/*收藏*/
	.fCollection {
	    display: -webkit-box;
	    display: -ms-flexbox;
	    display: flex;
	    -webkit-box-align: center;
	    -ms-flex-align: center;
	    align-items: center;
	    margin-top: 15px;
	    height: 24px;
	    font-size: 14px;
	    color: #8590a6;
	    font-weight: 500;
		
	}
	
	
	.banner{
		width: 100%;
		margin-bottom: 10px;
		margin-top: -10px;
		height: 60px;
		display: flex;
		align-items: center;
		font-size: 20px;
	}
	
	.box{
		display: flex;
		width: 1000px;
		    height: 179px;
		margin-bottom: 20px;
		padding: 25px;
		background-color: white;
		border-radius: 6px;
	}


</style>
