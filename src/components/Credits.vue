<template>
	<section>
		<div>
			<button>Sing-up Now</button>
			<nav>
				<h3>Follow Us</h3>
				<a href="#" v-for="(imageURL, index) in images" :key="index"
					><img :src="getImage(index)" alt="image"
				/></a>
			</nav>
		</div>
	</section>
</template>

<script>
export default {
	name: "Credits",
	data() {
		return {
			images: [
				"footer-facebook.png",
				"footer-twitter.png",
				"footer-youtube.png",
				"footer-pinterest.png",
				"footer-periscope.png",
			],
		};
	},
	methods: {
		getImage(index) {
			return require(`../assets/images/${this.images[index]}`);
		},
	},
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/variable.scss";

section {
	padding: 1rem;
	background: $gray-700;

	> div {
		@include container;

		button {
			color: $white;
			cursor: pointer;
			font-weight: 600;
			font-size: 0.75rem;
			line-height: 1.25rem;
			background: $gray-700;
			letter-spacing: 0.02rem;
			padding: 0.5rem 0.625rem;
			text-transform: uppercase;
			border: 3px solid $blue-500;
		}

		nav {
			display: flex;
			align-items: center;

			> * {
				margin: 0 0.5rem;
			}

			h3 {
				color: $blue-500;
				font-size: 1.25rem;
				margin-right: 1rem;
				text-transform: uppercase;
			}

			a {
				width: 2rem;
				height: 2rem;
				display: flex;
				flex-shrink: 0;

				&:hover > img {
					filter: invert(36%) sepia(39%) saturate(3599%)
						hue-rotate(193deg) brightness(99%) contrast(98%);
				}
			}
		}
	}
}
</style>
