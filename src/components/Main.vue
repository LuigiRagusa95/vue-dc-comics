<template>
	<main>
		<Series />
	</main>
</template>

<script>
import Series from "./Series.vue";

export default {
	components: { Series },
	name: "Main",
	data() {
		return {
			message: "--> Content goes here <--",
		};
	},
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/variable.scss";

main {
	flex-grow: 1;
	display: flex;
	flex-flow: column;
	background-color: $gray-800;

	> div {
		@include container;

		.message {
			color: $white;
			font-weight: 600;
			font-size: 1.5rem;
		}
	}
}
</style>
