<script setup>
	import Tmp from "./components/AttrBind.vue"
	import AttrBind from "./components/Tmp.vue"
</script>

<template>
	<!-- 显示组件 -->
  <Tmp style="border: 2px solid black;"></Tmp>
  <AttrBind style="border: 1px solid green;"></AttrBind>
 
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
