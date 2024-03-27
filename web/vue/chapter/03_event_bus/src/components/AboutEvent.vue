<template>
  <div class="about-event">
		About
		<button @click="btnClick">单击按钮 触发事件</button>
  </div>
</template>

<script>
	import emitter from '../utils/EventBus'
	
export default {
	methods: {
		btnClick() {
			console.log("1.About 页面的： 单击按钮->触发全局why事件");
			emitter.emit("why", {name:"why", age:18});
			
			console.log("3.About 页面的： 单击按钮->触发全局kobe事件");
			emitter.emit("kobe", {name:"kobe", age:26});
		}
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
