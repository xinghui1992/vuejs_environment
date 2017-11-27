<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <ul>
      <li><a href="https://github.com/xinghui1992/vuejs_environment" target="_blank">GitHub</a></li>
      <li><a href="https://segmentfault.com/u/gehui" target="_blank">SegmentFault</a></li>
    </ul>
    <h2>Relevant Document</h2>
    <ul>
      <li @click="router">vue-router</li>
      <li><a href="http://vuex.vuejs.org/" target="_blank">vuex</a></li>
      <li><a href="http://vue-loader.vuejs.org/" target="_blank">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank">awesome-vue</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Rastar Group App'
    }
  },
  mounted() {},//配置相关页面加载进入执行的方法
	methods:{
		router(){
			this.$router.push({name:'Router'});
		}
	},//页面相关调用的方法
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
