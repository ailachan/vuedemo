<!-- 
属性绑定 
 -->

<template>
	
	<div>
		<!-- v-bind这是一个属性绑定的vue指令，将数据添加为属性的值 -->
		<div v-bind:id="divID">测试文本</div>
		<!-- 简写形式，v-bind可以省略 -->
		<div :name="divID">测试文本</div>
		<!-- 布尔型属性，一般用值控制这个属性是否生效，
			html中有一类属性，只有生效或者不生效两种状态，没有取值
			比如disabled,readonly属性，
			这里可以使用布尔型绑定来控制，
		 -->
		 <input type="text" :readonly="enableStatus"
		    :disabled="enableStatus" />
			
		<!-- 动态绑定多个值 :同时绑定多个属性值 -->
		<div v-bind="objectOfAttrs">测试文本</div>
		
	</div>
	
</template>

<script>
	export default{
		data(){
			return{
				divID:"myDiv",
				enableStatus:true,
				objectOfAttrs: {
				  id: 'container',
				  class: 'wrapper'
				}
			}
		}
	}
</script>

<style>
</style>