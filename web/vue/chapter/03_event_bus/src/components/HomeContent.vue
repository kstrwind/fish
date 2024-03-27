<template>
	<div class="home-content">
		HomeContent
	</div>
</template>

<script>
	import emitter from "@/utils/EventBus";
	export default {
		name:"homeContent",
		created() {
			emitter.on("why", (info) => {
				console.log("why:", info);
			});
			emitter.on("kobe", (info) => {
				console.log("kobe:", info);
			});
			emitter.on("*", (type, info) => {
				console.log("* listener:", type, info);
			});
		},
	}
</script>

<style>
</style>