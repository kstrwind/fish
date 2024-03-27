<template>
	<div class="app">
		App
		<home-page/>
		<about-event/>
	</div>
</template>

<script>
import HomePage from './components/HomePage.vue';
import AboutEvent from './components/AboutEvent.vue';

export default {
  name: 'App',
  components: {
    HomePage,
		AboutEvent,
  }
}
</script>

<style>

</style>
