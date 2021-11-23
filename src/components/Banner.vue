<template>
	<section>
		<div>
			<ul>
				<li v-for="(link, index) in list" :key="index">
					<a href="#"
						><img
							:src="require(`../assets/images/${link.img}`)"
							alt="image"
						/><span>{{ link.title }}</span></a
					>
				</li>
			</ul>
		</div>
	</section>
</template>

<script>
export default {
	name: "Banner",
	data() {
		return {
			// prettier-ignore
			list: [
				{ title: "Digital Comics",img: "buy-comics-digital-comics.png", },
				{ title: "DC Merchandise", img: "buy-comics-merchandise.png" },
				{ title: "Subscription", img: "buy-comics-subscriptions.png" },
				{ title: "Comic Shop Locator",img: "buy-comics-shop-locator.png", },
				{ title: "DC Power Visa", img: "buy-dc-power-visa.svg" },
			],
		};
	},
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
