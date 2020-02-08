<template>
	<div>
		<div class="container">
			<div class="row">
				<div class="banner">
					<i class="iconfont">&#xe670;</i>
					<h3>全部专题</h3>
				</div>
				<div class="col-12 box" v-for="(item,index)  in specials" v-if="index>begin&&index<end" :key="index">
						<div class="box-left"><img :src="item.banner" alt=""></div>
						<div class="box-right">
							<div class="box-head">
							<div class="left">
							<h3>{{item.title}}</h3>
							<p class="meta">{{item.updated}}更新,{{item.viewCount}}次浏览</p>
							</div>
							<div class="right">
								<button class="btn_gz">关注专题</button>
							</div>
							</div>
							<div class="box-body">
								<p class="introduction">{{item.introduction}}</p>
							</div>
							<div class="box-bottom">
								<span v-for="(section,index) in item.sections" :key="index" class="section flex">
									{{section.sectionTitle}}
								</span>
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
			specials:[],
			begin:0,
			end:6,
		};
	},
	created() {
		this.axios.get('http://localhost:8080/api/special/all').then(res =>{
			console.log(res);
			this.specials = res.data.data;
		});
	},
	methods: {
	show_all(){
	this.begin=0;
	this.end =this.specials.length;
	}						
	},					
};
</script>

<style  lang="scss" scoped>
	.banner{
		width: 100%;
		margin-bottom: 10px;
		margin-top: -10px;
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
	.box{
		display: flex;
		width: 100%;
		height: 220px;
		margin-bottom: 20px;
		padding: 25px;
		background-color: white;
		border-radius: 6px;
	}
	.box-left{
		width: 35%;
		margin-right: 20px;
		img{
			width: 100%;
			height: 100%;
			border-radius: 3px;
		}
	}
	.box-right{
		width: 65%;
		position: relative;
	}
	.box-head{
		display: flex;
	}
	.left{
		width: 83%;
	}
	.right{
		width: 17%;
		margin-bottom: 30px;
	}
	.box-bottom{
		display: flex;
		position: absolute;
		left: 0;
		bottom: 0;
	}
	.section{
		padding: 0 8px;
		height: 24px;
		line-height: 24px;
		border-radius: 5px;
		background-color: #f6f6f6;
		color: #8590a6;
		font-size: 12px;
		margin-right: 13px;
	}
	
	.introduction{
		display: flex;
	}
</style>
