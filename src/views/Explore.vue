<template>
	<div>
		<div class="container">
			<div class="row">
				<div class="banner">
					<i class="iconfont">&#xe670;</i>
					<h3>最新专题</h3>
				</div>
				<div class="col-6 card" v-for="(item,index) in specials" :key="index">
						<div class="card-head"><img :src="item.banner" alt=""></div>
						<div class="card-body flex">
							<div class="left">
							<h3>{{item.title}}</h3>
							<p class="meta">{{item.updated}}更新,{{item.viewCount}}次浏览</p>
							</div>
							<div class="right">
								<button class="btn_gz">关注专题</button>
							</div>
							<p class="introduction">{{item.introduction}}</p>
						</div>
						<div class="card-buttom">
						<span v-for="(section,index) in item.sections" :key="index" class="section flex">
							{{section.sectionTitle}}
						</span>
						</div>
					</div> 
					<div class="center"><router-link to="/special/all" class="l">查看更多专题 ></router-link></div>
			</div>
			<div class="row">
				<div class="banner">
					<i class="iconfont">&#xe639;</i>
					<h3>圆桌讨论</h3>
				</div>
				<div class="col-6 card" v-for="(item,index) in roundTables" :key="index">
						<div class="cards-head">
							<div class="card-background">
								<img :src="item.banner" alt="">
							</div>
							<div class="card-main">
								<p class="name">{{item.name}}</p>
								<p>{{item.visitsCount}}人访问,{{item.includeCount}}人参与</p>
							</div>
							<div class="card-btn">
								<button class="btn_gz">关注圆桌</button>
							</div>
							</div>
						<div class="card-body flex">
							<p class="introduction">{{item.urlToken}}</p>
						</div>
						<div class="card-buttom">
						<span v-for="(section,index) in item.sections" :key="index" class="section flex">
							{{section.sectionTitle}}
						</span>
						</div>
					</div> 
					<div class="center"><router-link to="/roundTable/all" class="l">查看更多圆桌></router-link></div>
			</div>
			<div class="row">
				<div class="banner">
					<i class="iconfont"><svg class="Zi Zi--Star" fill="currentColor" viewBox="0 0 24 24" width="36" height="36"><path d="M5.515 19.64l.918-5.355-3.89-3.792c-.926-.902-.639-1.784.64-1.97L8.56 7.74l2.404-4.871c.572-1.16 1.5-1.16 2.072 0L15.44 7.74l5.377.782c1.28.186 1.566 1.068.64 1.97l-3.89 3.793.918 5.354c.219 1.274-.532 1.82-1.676 1.218L12 18.33l-4.808 2.528c-1.145.602-1.896.056-1.677-1.218z" fill-rule="evenodd"></path></svg></i>
					<h3>热门收藏夹</h3>
				</div>
				<div class="col-61 card" v-for="(item,index) in  favorite" :key="index">
						<div class="card-fhead ">
								<p class="card-p">{{item.title}}</p>
								<div class="card-fuserimage flex">
									<img :src="item.creatorAvatar" alt="">
									<p class="fp">{{item.creatorName}}  <a class="chuangjian">创建</a>&nbsp;&nbsp;</p>
									<div class="fg">
										{{item.followers}}关注
									</div>
									<div class="card-fbtn" alt="">
									<button class="btn_fgz">关注收藏夹</button>
																	
									</div>
									</div>
								</div>
								
								
								
								<div class="slist">
									<br />
									<hr style="border:0;background-color:#ebebeb;height:1px;"> 
									<br />
									<div class="sitem">
										<a class="stitle" href="#" >{{item.questionTitle}}</a>
										<div class="stext">{{item.answerAuthorName}}:{{item.answerContent}}</div>
										<div class="stags">
										<span class="stagss">回答 </span>
										<span class="stag">{{item.voteupCount}}赞同</span >
										<span class="stag">{{item.commentCount}}评论</span >
										</div>
										
										</div>
										
										<br />
										<div class="sitem">
										<a class="stitle" href="#" >{{item.questionTitle}}</a>
										<div class="stext">{{item.answerAuthorName}}:{{item.answerContent}}</div>
										<div class="stags">
										<span class="stagss">回答</span>
										<span class="stag">{{item.voteupCount}} 赞同</span>
										<span class="stag">{{item.commentCount}} 评论</span>
										
										</div>
										</div>
										</div>
										
								<a class="ExploreCollectionCard-collectedContentCount" href="/collection/73043547" target="_blank" rel="noopener noreferrer" data-za-detail-view-id="5804" data-za-detail-view-name="已收藏点击">已收藏 235 条内容<svg class="Zi Zi--ArrowRight" fill="currentColor" viewBox="0 0 24 24" width="24" height="24"><path d="M9.218 16.78a.737.737 0 0 0 1.052 0l4.512-4.249a.758.758 0 0 0 0-1.063L10.27 7.22a.737.737 0 0 0-1.052 0 .759.759 0 0 0-.001 1.063L13 12l-3.782 3.716a.758.758 0 0 0 0 1.063z" fill-rule="evenodd"></path></svg></a>
							
						
							</div>
				
				
					<div class="center"><router-link to="/favorite/all" class="l">查看更多收藏></router-link></div>
					
								
			</div>
				<div class="row">
								<div class="banner">
									<i class="iconfont">
				<svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--EditCircle" fill="currentColor" viewBox="0 0 24 24" width="36" height="36"><path fill-rule="evenodd" d="M 12 22 C 6.477 22 2 17.523 2 12 S 6.477 2 12 2 s 10 4.477 10 10 s -4.477 10 -10 10 Z m 4.043 -15.524 a 0.745 0.745 0 0 0 -1.053 0.017 l -6.857 7.071 l 2.237 2.17 l 6.857 -7.071 a 0.743 0.743 0 0 0 -0.016 -1.052 l -1.168 -1.135 Z m -9.028 9.476 l -0.348 1.381 l 1.37 -0.39 l 1.274 -0.36 l -1.973 -1.916 l -0.323 1.285 Z" /></svg>						</i>
									<h3>专栏</h3>
								</div>
								<div class="col-62 card" v-for="(item,index) in  columns" :key="index">
										<div class="card-zhead ">
												
												<div class="card-zuserimage flex">
													<img :src="item.imageUrl" alt="">
													
												
													</div>
												</div>
												
												
												
												
													<div class="zitem">
														<a class="ztitle" href="#" >{{item.title}}</a>
														<div class="zfollowersrard">
															<span class="zfollowers">{{item.followers}} 关注</span>
															
															<span> {{item.articlesCount}} 文章</span>
														</div>
														<div class="ztext">
														{{item.description}}
														</div>
														
													<div class="card-zbtn" alt="">
													<button class="btn_zgz">关注收藏夹</button>
																					
													</div>
										
									</div>
									
									
							</div>
							<div class="center"><router-link to="/columns/all" class="l">查看更多专栏></router-link>
							<br>
							<br>
							<br>
							<br>
							<br>
							<br>
							<br>
							<br>
							<br>
							</div>	
							</div>	
		</div>
	</div>
</template>

<script>
export default{
	name:'special',
	data(){
		return{
			specials:[],
			roundTables:[],
			favorite:[],
			columns:[],
		};
	},
	created() {
		this.axios.get('http://localhost:8080/api/special').then(res =>{
			console.log(res);
			this.specials = res.data.data;
		});
		this.axios.get('http://localhost:8080/api/roundTable').then(res =>{
			console.log(res);
			this.roundTables = res.data.data;
		});
		this.axios.get('http://localhost:8080/api/favorite').then(res =>{
			console.log(res);
			this.favorite = res.data.data;
		});
		this.axios.get('http://localhost:8080/api/columns').then(res =>{
				console.log(res);
				this.columns = res.data.data;
			});
		
	}
};
</script>

<style  lang="scss" scoped>
	.banner{
		width: 100%;
		margin-bottom: 10px;
		margin-top: 10px;
		height: 60px;
		display: flex;
		align-items: center;
		font-size: 20px;
	}
	.iconfont{
		color: rgb(0,132,255);
		font-size: 32px;
		margin-right:10px;
	}
	.left{
		width: 60%;
	}
	.right{
		width: 100px;
		margin-left: 50px;
		margin-bottom: 30px;
	}
	.card{
		background-color: rgb(255,255,255);
		// border: 1px solid #d6d6d6;
		box-shadow: 0 1px 3px 0 rgba(26,26,26,.1);
		border-radius: 4px;
		width: 490x;
		height: 450px;
		margin-right: 20px;
		margin-bottom: 25px;
		padding-bottom: 5px;
	}	
	.cards-head{
		position: relative;
		height: 240px;
		background-image: linear-gradient(to right, rgb(0, 0, 255) 0%, rgba(0, 0, 255, 0) 100%);
	}
	.card-background{
		position: absolute;
		top: 0;
		right: 0;
		bottom: 0;
		width: 240px;
	}
	.card-main{
		position: relative;
		width: 320px;
		padding: 68px 24px 24px;
	}
	.card-btn{
		position: absolute;
		right: 24px;
		bottom: 24px;
		background-color: white;
		border-radius: 5px;
	}
	.card-body{
		margin: 18px;
	}
	.btn_gz{
		-webkit-tap-highli0ht-color: rgba(26,26,26,0);
		font: inherit;
		cursor: pointer;
		background: none;
		border: none;
		outline: none;
		-webkit-appearance: none;
		height: 34px;
		border-radius: 3px;
		font-size: 14px;
		font-weight: 600;
		width: 102px;
		color: #0084ff;
		background-color: rgba(0,132,255,.08);
		
	}
	.introduction{
		border-top: 1px solid #ebebeb;
		margin-top: 5px;
		padding-top: 14px;
		display: flex;
	}
	.name{
		font-size: 28px;
		font-weight: 660;
		color: white;
		margin-bottom: 30px;
	}
	.col-6{
		flex: 0 0 48%;
		img{
			width: 100%;
			height: 100%;
			padding: 2px;
			border-bottom-left-radius: 4px;
			border-bottom-right-radius: 4px;
		}
	}
	
	
	.col-61{
			    width: 480px;
			    height: 364px;
			}
		
		.card-fuserimage{
		
					 position: absolute;
					 top: 70px;
					 left: 25px;
			
			img{
				width: 8%;
			}
		}
		.btn_fgz{
			-webkit-tap-highli0ht-color: rgba(26,26,26,0);
			font: inherit;
			cursor: pointer;
			background: none;
			border: none;
			outline: none;
			-webkit-appearance: none;
			height: 34px;
			border-radius: 3px;
			font-size: 14px;
			font-weight: 600;
			width: 102px;
			color: #0084ff;
			background-color: rgba(0,132,255,.08);
			
		}
		.card-fhead{
			position: relative;
			
			   
			   
		}
	   .card-fbtn{
		   position: absolute;
		   top: -40px;
		left: 320px;
		border-radius: 5px;
		bottom: 24px;
	}
	     .card-p{
			  position: absolute;
			     height: 28px;
			     line-height: 28px;
			     font-size: 20px;
			     overflow: hidden;
			     text-overflow: ellipsis;
			     white-space: nowrap;
			     font-weight: 600;
				 margin-top: 30px;
				 margin-left: 30px;
				 
		 }
		 .fg{
			     margin-left: 7px;
			     padding-left: 7px;
			     height: 19px;
			     line-height: 19px;
			     font-size: 14px;
			     color: #999;
			     border-left: 2px solid #ebebeb;
		 }
		 .fp{
			 
			margin-left: 4px;
			padding-left: 4px;
			height: 19px;
			line-height: 19px;
			font-size: 14px; 
		 }
		 .chuangjian{
			 
			 color: #999;
		 }
	       /*收藏置顶标题*/
		 .stitle {	
			 color: black;
		     display: block;
		     height: 21px;
		     line-height: 21px;
		     overflow: hidden;
		     text-overflow: ellipsis;
		     font-weight: 600;
		     font-synthesis: style;
		 }
		  /*收藏置顶内容*/
		 .stext {
			 
		        margin-top: 4px;
	    height: 21px;
	    line-height: 21px;
	    color: #444;
	    
	    overflow: hidden;
	    text-overflow: ellipsis;
		 }
		 /*收藏置顶赞同评论·*/
		 .stag {
		     height: 20px;
		     line-height: 20px;
		     padding: 0 4px;
		     
		     color: #999;
		     font-size: 12px;
		     margin-right: 8px;
		 }
		  /*收藏置顶回答*/
		 .stagss{
			 height: 20px;
			 line-height: 20px;
			 padding: 0 4px;
			 
			 color: #999;
			 font-size: 12px;
			 margin-right: 8px;
			   background-color: #f6f6f6;
		 }
		 /*收藏置顶赞同和评论数*/
		 .stags span {
		     -ms-flex-negative: 0;
		 		
		     flex-shrink: 0;
		 }
		 /*收藏置顶赞同和评论数*/
		 .ExploreCollectionCard-contentCountTag {
		     height: 17px;
			 
		     line-height: 17px;
		     font-size: 12px;
		     color: #999;
		 }
		 
		 .slist {
			
		     margin: 100px 24px;
		     height: 110px;
		 }
		  /*收藏置顶已收藏内容*/
	.ExploreCollectionCard-collectedContentCount {
		border-top: 1px solid #ebebeb;
		margin-top: 5px;
		padding-top: 14px;
		display: flex;
	    display: -webkit-box;
	    display: -ms-flexbox;
	    display: flex;
	    -webkit-box-align: center;
	    -ms-flex-align: center;
	    align-items: center;
	    margin: 20px 24px 0;
	    height: 24px;
	    font-size: 14px;
	    color: #8590a6;
	    font-weight: 600;
	    font-synthesis: style;
	}
	
	
	.col-62{
		display: flex;
		    -webkit-box-orient: vertical;
		    -webkit-box-direction: normal;
		    -ms-flex-direction: column;
		    flex-direction: column;
		align-items: center;
		text-align: center;
		padding: 28px 24px;
		width: 20px;
		height: 313px;
		
		
	}
	.card-zhead{
		display: block; 
		
		    width: 80px;
		    height: 80px;
	}
	.card-zuserimage{
		
		img{
		width: 100%;
		    height: 100%;
		    border-radius: 50%;
			
			}
	}
	.zitem{
		margin-top: 20px;
	}
	.ztitle{
		text-align: center;
	
		  
			color: black;
		  
		    font-weight: 600;
			padding: 28px 24px;
		   
			align-items: center;
			
	}
	.zfollowersrard{
		
		margin-top: 6px;
		    height: 17px;
			
		    
		    font-size: 12px;
		    color: #999;
	}
	.zfollowers{
		margin-top: 4px;
		    height: 17px;
			
		    line-height: 17px;
		    font-size: 12px;
		    color: #999;
	}
	.ztext{
		
		margin-top: 20px;
	    height: 40px;
	    line-height: 20px;
	    font-size: 14px;
	    color: #444;
	    text-align: center;
	    display: -webkit-box;
	    text-overflow: ellipsis;
	    overflow: hidden;
	    -webkit-line-clamp: 2;
	    -webkit-box-orient: vertical;
	}
	.btn_zgz{
			-webkit-tap-highli0ht-color: rgba(26,26,26,0);
			font: inherit;
			cursor: pointer;
			background: none;
			border: none;
			outline: none;
			-webkit-appearance: none;
			height: 34px;
			border-radius: 3px;
			font-size: 14px;
			font-weight: 600;
			width: 102px;
			color: #0084ff;
			background-color: rgba(0,132,255,.08);
			
		}
		
	   .card-zbtn{
		  margin-top: 20px;
		border-radius: 5px;
		bottom: 24px;
	}
</style>
