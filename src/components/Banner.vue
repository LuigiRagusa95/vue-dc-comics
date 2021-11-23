<template>
	<section>
		<div>
			<ul>
				<li>
					<a href="#"
						><img
							src="../assets/images/buy-comics-digital-comics.png"
							alt="image"
						/><span>Digital Comics</span></a
					>
				</li>
				<li>
					<a href="#"
						><img
							src="../assets/images/buy-comics-merchandise.png"
							alt="image"
						/><span>DC Merchandise</span></a
					>
				</li>
				<li>
					<a href="#"
						><img
							src="../assets/images/buy-comics-subscriptions.png"
							alt="image"
						/><span>Subscription</span></a
					>
				</li>
				<li>
					<a href="#"
						><img
							src="../assets/images/buy-comics-shop-locator.png"
							alt="image"
						/><span>Comic Shop Locator</span></a
					>
				</li>
				<li>
					<a href="#"
						><img
							src="../assets/images/buy-dc-power-visa.svg"
							alt="image"
						/><span>DC Power Visa</span></a
					>
				</li>
			</ul>
		</div>
	</section>
</template>

<script>
export default {
	name: "Banner",
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/variable.scss";

section {
	width: 100%;
	color: $white;
	padding: 1rem;
	background: $blue-500;

	> div {
		@include container;

		ul {
			width: 100%;
			display: flex;
			align-items: center;
			justify-content: space-between;

			> li {
				padding: 1rem;

				a {
					display: flex;
					align-items: center;
					text-transform: uppercase;

					img {
						width: 56px;
						height: 56px;
						object-fit: contain;
						margin-right: 1rem;
					}

					span {
						display: flex;
						font-size: 1rem;
						line-height: 1.5rem;
						margin-right: 0.5rem;
					}
				}
			}
		}
	}
}
</style>
