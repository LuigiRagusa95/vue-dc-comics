<template>
	<section>
		<div>
			<div class="section-label">Current Series</div>
			<div class="section-grid">
				<template v-for="(element, index) in list">
					<Card
						:key="`card-${index}`"
						:thumb="element.thumb"
						:series="element.series"
					/>
				</template>
			</div>
			<div class="section-button">Load More</div>
		</div>
	</section>
</template>

<script>
import productList from "../data/cards.js";
import Card from "./Card.vue";

export default {
	name: "Series",
	components: {
		Card,
	},
	data() {
		return {
			list: productList,
		};
	},
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/variable.scss";
section {
	display: flex;
	min-height: 400px;
	position: relative;

	> div:first-of-type {
		@include container();
		flex-direction: column;
		align-items: flex-start;

		.section-label {
			color: $white;
			font-size: 1rem;
			font-weight: 600;
			position: absolute;
			line-height: 1.5rem;
			padding: 0.5rem 1rem;
			background: $blue-500;
			text-transform: uppercase;
			bottom: calc(100% - ((1.5rem + 1rem) / 2));
		}

		.section-grid {
			width: 100%;
			display: flex;
			padding: 1rem;
			flex-wrap: wrap;
			margin-top: 2rem;
			align-items: flex-start;
		}

		.section-button {
			color: $white;
			cursor: pointer;
			font-weight: 600;
			width: fit-content;
			margin: 0 auto 2rem;
			padding: 0.75rem 3rem;
			background: $blue-500;
		}
	}
}
</style>
