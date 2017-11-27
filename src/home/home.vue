<template>
	<div data-page="router">
		<h2>文件配置</h2>
		<h4>页面结构</h4>
		<ul class="items_list">
			<li v-for="(item,index) in items" @click="itemList(index)">{{item}}</li>
		</ul>
		<ul>
			<li></li>
			<li></li>
			<li></li>
		</ul>
	</div>
</template>

<script>
	export default {
	  name: 'HelloWorld',
	  data () {
	  	return {
	      items: ['template','script','style'],
	    }
	  },
	  mounted() {
	  	this.init();
	  },//配置相关页面加载进入执行的方法
		methods:{
			init(){
				var $li=$('.items_list li');
				$li[0].className='active';
			},
			itemList(index){
				var $li=$('.items_list li');
				$li.removeClass('active');
				$li[index].className='active';
			}
		},//页面相关调用的方法
	}
</script>

<style>
	.items_list{
		overflow: hidden;
		display: flex;
		padding: 0;
	}
	.items_list li{
		list-style: none;
		float: left;
		text-align: center;
		margin: auto;
		flex: 1;
		color:#737373;
		padding: 10px 0;
	}
	.items_list li.active{
		color: #6296ff;
		border-bottom: 2px solid #6296FF;
	}
</style>