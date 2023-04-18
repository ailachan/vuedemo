<!-- 
	vue组件中的三个核心之一，我们成为模板，实际上就是html
	（这部分最后会被编译为js），html决定了显示的内容
 -->
<template>
	<h1>模板语法</h1>
	<!-- 插值表达式显示vue中定义的数据,{{}}是纯文本插入 -->
	<div>{{msg}}</div>
	<!-- html插入,v-html这个东西我们称为vue指令，实际上是vue自定一的属性，
	 一般是支持某些特定功能的，比如说这里，代表html插入
	 -->
	<div v-html="spn"></div>
</template>

<!-- 
 script添加我们的js代码，这个写代码主要用于定义数据，方法，事件，前后端交互
 只在本组件生效，可以理解为与template模板对应
 -->
<script>
	export default {
		//定义数据
		data(){
			return{
				msg:"hello vue",
				spn:`
					<div style="color:red;">
						<p>测试文本</p>
					</div>
				`
			}
		}
	}
</script>

<!-- 添加css样式，加一个scoped,带表只在本组件有效 -->
<style scoped>
	h1{
		color: red;
		background-color: aliceblue;
	}
	
</style>