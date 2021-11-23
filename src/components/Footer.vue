<template>
	<footer>
		<div>
			<section>
				<div class="column">
					<ul>
						<li><h2>DC Comics</h2></li>
						<li><a href="#">Characters</a></li>
						<li><a href="#">Comics</a></li>
						<li><a href="#">Movies</a></li>
						<li><a href="#">Tv</a></li>
						<li><a href="#">Games</a></li>
						<li><a href="#">Videos</a></li>
						<li><a href="#">News</a></li>
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
						<li><a href="#">Terms Of Use</a></li>
						<li><a href="#">Privacy Policy</a></li>
						<li><a href="#">Ad Choices</a></li>
						<li><a href="#">Advertising</a></li>
						<li><a href="#">Jobs</a></li>
						<li><a href="#">Subscriptions</a></li>
						<li><a href="#">Talent Workshops</a></li>
						<li><a href="#">CPSC Certificates</a></li>
						<li><a href="#">Ratings</a></li>
						<li><a href="#">Shop Help</a></li>
						<li><a href="#">Contact Us</a></li>
					</ul>
				</div>
				<div class="column">
					<ul>
						<li><h2>Sites</h2></li>
						<li><a href="#">DC</a></li>
						<li><a href="#">MAD Magazine</a></li>
						<li><a href="#">DC Kids</a></li>
						<li><a href="#">DC Universe</a></li>
						<li><a href="#">DC Power Visa</a></li>
					</ul>
				</div>
			</section>
			<section>
				<img src="../assets/images/dc-logo-bg.png" alt="image" />
			</section>
		</div>
	</footer>
</template>

<script>
export default {
	name: "Footer",
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/variable.scss";

footer {
	flex-grow: 1;
	color: $white;
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
