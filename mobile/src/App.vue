<template>
	<div id="app">
		<router-view/>

		<!-- 底部tab切换 -->
		<mt-tabbar v-model="tabIndex" fixed>
			<mt-tab-item id="/">
				<span class="fa fa-home"></span> 首页
			</mt-tab-item>
			<mt-tab-item id="/client">
				<span class="fa fa-group"></span> 招生
			</mt-tab-item>
			<mt-tab-item id="/add">
				<span class="fa fa-plus"></span> 新增
			</mt-tab-item>
			<mt-tab-item id="/serive">
				<span class="fa fa-address-book"></span> 教务
			</mt-tab-item>
			<mt-tab-item id="/user">
				<span class="fa fa-user"></span> 我的
			</mt-tab-item>
		</mt-tabbar>
	</div>
</template>


<script>
	export default {
		data() {
			return {
				tabIndex: '/'
			};
		},
		watch:{
			tabIndex(val){
				 this.$router.push(val);
			}
		},
		components: {}
	}
</script>


<style>
	html {
		font-size: calc(100vw/7.5);
	}
	
	body {
		margin: 0;
		font-family: "arial, helvetica, sans-serif";
		font-size: 0.14rem;
		color: #333;
	}
	
	html,
	body,
	#app {
		width: 100%;
		height: 100%;
	}
	
	.left {
		float: left;
	}
	
	.right {
		float: right;
	}
	
	.clear:after {
		display: block;
		content: "";
		clear: both;
	}
	
	.flex {
		display: flex;
	}
	
	.flex-item {
		flex: 1;
	}
	
	.flex-column {
		flex-flow: column;
	}
	
	a {
		text-decoration: none;
		color: #333333;
	}
	
	ul,
	ol {
		margin: 0;
		padding: 0;
		list-style: none;
	}
	
	img {
		border: 0 none;
		vertical-align: top;
	}
	
	.mint-tabbar {
		box-shadow: 0 0 10px 0 hsla(0, 6%, 58%, .6);
		-webkit-box-shadow: 0 0 10px 0 hsla(0, 6%, 58%, .6);
		-moz-box-shadow: 0 0 10px 0 hsla(0, 6%, 58%, .6);
	}
	
	.mint-tabbar .fa {
		display: block;
		font-size: 0.4rem;
		margin-bottom: .1rem;
	}
</style>