<template>
	<section>
		<div>
			<button>Sing-up Now</button>
			<nav>
				<h3>Follow Us</h3>
				<a href="#"
					><img
						src="../assets/images/footer-facebook.png"
						alt="image"
				/></a>
				<a href="#"
					><img src="../assets/images/footer-twitter.png" alt="image"
				/></a>
				<a href="#"
					><img src="../assets/images/footer-youtube.png" alt="image"
				/></a>
				<a href="#"
					><img
						src="../assets/images/footer-pinterest.png"
						alt="image"
				/></a>
				<a href="#"
					><img
						src="../assets/images/footer-periscope.png"
						alt="image"
				/></a>
			</nav>
		</div>
	</section>
</template>

<script>
export default {
	name: "Credits",
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
