<template>
	<div class="tab-control">
    <div v-for="(title, index) in titles" 
			class="tab-control-item"
			:class="{active: currentIndex === index}"
			:key="title"
			@click="itemClick(index)">
			<span>{{title}}</span>
		</div>
  </div>
</template>

<script>
export default {
	emits:["titleClick"],
	props:{
		titles: {
			type:	Array,
			default() {
				return []
			}
		}
	},
	data() {
		return {
			currentIndex: 0
		}
	},
	methods: {
		itemClick(index) {
			this.currentIndex = index;
			this.$emit("titleClick", index);
		}
	},
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	.tab-control {
		display: flex;
	}
	.tab-control-item {
		flex: 1;
		text-align: center;
	}
	.tab-control-item.active {
		color: red;
	}
	.tab-control-item.active span {
		border-bottom: 3px solid red;
		padding: 5px 10px;
	}
</style>

