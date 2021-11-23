<template>
	<main>
		<div class="container">
			<div>
				<section>
					<p class="message">{{ message }}</p>
				</section>
			</div>
		</div>
		<Banner />
	</main>
</template>

<script>
import Banner from "./Banner.vue";

export default {
	name: "Main",
	components: {
		Banner,
	},
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

		> div {
			width: 100%;
			display: flex;
			flex-flow: column;

			.message {
				color: $white;
				font-weight: 600;
				font-size: 1.5rem;
			}
		}
	}
}
</style>
