<template>
	<div class="card">
		<div class="card-image">
			<div>
				<img :src="thumb" :alt="series" />
			</div>
		</div>
		<div class="card-title">
			<span>{{ series }}</span>
		</div>
	</div>
</template>

<script>
export default {
	name: "Card",
	props: {
		thumb: String,
		series: String,
	},
	data() {
		return {};
	},
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/variable.scss";
.card {
	width: 100%;
	display: flex;
	cursor: pointer;
	flex-flow: column;
	padding: 0.25rem;
	margin-bottom: 1rem;
	width: calc(100% / 6);

	.card-image {
		> div {
			width: 100%;
			overflow: hidden;
			position: relative;
			padding-bottom: calc(100% * 1);

			img {
				top: 0;
				left: 0;
				width: 100%;
				object-fit: cover;
				position: absolute;
			}
		}
	}

	.card-title {
		padding: 1rem 0;
		font-size: 1rem;
		color: $gray-500;
		line-height: 1.5rem;

		> span:first-of-type {
			display: block;
			overflow: hidden;
			font-weight: 600;
			white-space: nowrap;
			text-overflow: ellipsis;
			text-transform: uppercase;
		}
	}
}
</style>
