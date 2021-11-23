<template>
	<footer>
		<div>
			<section>
				<div class="column">
					<ul>
						<li><h2>DC Comics</h2></li>
						<li
							v-for="(menu, index) in dcComicsMenuList"
							:key="index"
						>
							<a href="#">{{ menu }}</a>
						</li>
					</ul>
					<ul>
						<li><h2>Shop</h2></li>
						<li><a href="#">Shop DC</a></li>
						<li><a href="#">Shop DC Collectibles</a></li>
					</ul>
				</div>
				<div class="column">
					<ul>
						<li><h2>DC</h2></li>
						<li v-for="(menu, index) in dcMenuList" :key="index">
							<a href="#">{{ menu }}</a>
						</li>
					</ul>
				</div>
				<div class="column">
					<ul>
						<li><h2>Sites</h2></li>
						<li v-for="(menu, index) in dcSiteList" :key="index">
							<a href="#">{{ menu }}</a>
						</li>
					</ul>
				</div>
			</section>
			<section>
				<img src="../assets/images/dc-logo-bg.png" alt="image" />
			</section>
		</div>
		<Credits />
	</footer>
</template>

<script>
import Credits from "./Credits.vue";
export default {
	components: { Credits },
	name: "Footer",
	data() {
		return {
			dcComicsMenuList: [
				"Characters",
				"Comics",
				"Movies",
				"Tv",
				"Games",
				"Videos",
				"News",
			],
			dcMenuList: [
				"Terms Of Use",
				"Privacy Policy",
				"Ad Choices",
				"Advertising",
				"Jobs",
				"Subscriptions",
				"Talent Workshops",
				"CPSC Certificates",
				"Ratings",
				"Shop Help",
				"Contact Us",
			],
			dcSiteList: [
				"DC",
				"MAD Magazine",
				"DC Kids",
				"DC Universe",
				"DC Power Visa",
			],
		};
	},
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/variable.scss";

footer {
	display: flex;
	color: $white;
	flex-direction: column;
	justify-content: flex-end;
	background: url(../assets/images/footer-bg.jpg);

	> div:first-of-type {
		@include container;
		padding: 0;

		section {
			width: 100%;
			display: flex;

			.column {
				padding: 0.5rem;
				width: fit-content;

				ul {
					padding: 0.5rem;

					> li:first-of-type {
						font-size: 1rem;
						color: $gray-100;
						text-transform: uppercase;
					}

					> li {
						a {
							color: $gray-500;
							font-size: 0.875rem;
							line-height: 1.5rem;
							transition: color 0.1s ease;
						}
						&:hover > a {
							color: $white;
						}
					}
				}
			}

			&:last-of-type {
				overflow: hidden;
				max-height: 400px;
				align-items: center;
				justify-content: center;
			}
		}
	}
}
</style>
