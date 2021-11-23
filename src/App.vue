<template>
	<div id="app">
		<Header />
		<Main />
	</div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
export default {
	name: "App",
	components: {
		Header,
		Main,
	},
};
</script>

<style lang="scss">
@import "./assets/scss/reset.scss";
@import "./assets/scss/variable.scss";

#app {
	display: flex;
	flex-flow: column;
	min-height: 100vh;
}
</style>
