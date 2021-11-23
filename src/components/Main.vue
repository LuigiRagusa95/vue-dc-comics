<template>
	<main>
		<div>
			<p class="message">{{ message }}</p>
		</div>
	</main>
</template>

<script>
export default {
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
	background-color: $black;

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
