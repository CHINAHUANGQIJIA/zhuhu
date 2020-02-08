<template>
	<div>
		<div class="container">
			<div class="row">
				<div class="col-12 head flex flex-between">
					<div class="top-left-btn">
						<p>圆桌</p>
					</div>
					<div class="top-right-btn">
						<p>举办圆桌</p>
					</div>
				</div>
				<div class="col-3" v-for="(item,index)  in roundTables" v-if="index>begin&&index<end" :key="index">
					<div class="area">
						<div class="area-head">
							<img :src="item.banner" alt="">
							<p class="name">{{item.name}}</p>
						</div>
						<div class="area-body">
							<p>{{item.visits_count}}人访问,{{item.include_count}}人参与</p>
						</div>
					</div>
				</div>
			</div>
			<button @click="show_all" class="flex center l">展开全部>>></button>
		</div>
		<div><a href="#top" style="position: fixed; bottom: 5%; right: 5%;"><i class="iconfont" style="font-size: 30px;color: #0084FF;">&#xe633;</i></a></div>
	</div>
</template>

<script>
	export default {
		name: 'special',
		data() {
			return {
				roundTables: [],
				begin: 0,
				end: 13,
			};
		},
		created() {
			this.axios.get('http://localhost:8080/api/roundTable/all').then(res => {
				console.log(res);
				this.roundTables = res.data.data;
			});
		},
		methods: {
			show_all() {
				this.begin = 0;
				this.end = this.roundTables.length;
			}
		},
	};
</script>

<style lang="scss" scoped>
	.head {
		margin-bottom: 20px;
	}

	.row {
		width: 100%;
		margin: auto;
		margin-top: 10px;
		background-color: white;
		padding: 20px;
	}

	.top-left-btn {
		font-weight: 600;
		color: #1A1A1A;
		font-size: 15px;
		line-height: 20px;
	}

	.top-right-btn {
		color: #0084FF;
		font-weight: 600;
		font-size: 14px;
		line-height: 20px;
	}

	.col-3 {
		flex: 0 0 25%;

		img {
			height: 100%;
			width: 100%;
			border-radius: 6px;

		}
	}

	.area {
		margin-bottom: 30px;
		border-radius: 5px;
		padding-left: 25px;
		padding-right: 25px;
		margin-top: 20px;
		height: 240px;
	

		img {
			border-radius: 5px;
			
		}
	}

	.area-head {
		height: 80%;
		position: relative;
	}

	.area-body {
		height: 20%;
		background-color: white;
		padding: 10px;
		font-size: 14px;
		width: 100%;
		color: #778087;
	}

	.name {
		position: absolute;
		bottom: 5%;
		left: 5%;
		color: white;
	}
</style>
