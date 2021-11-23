<template>
	<header>
		<div>
			<div class="logo">
				<img src="../assets/images/dc-logo.png" alt="dc-logo-image" />
			</div>
			<nav class="navigation">
				<ul>
					<li><a href="#">Characters</a></li>
					<li class="active"><a href="#">Comics</a></li>
					<li><a href="#">Movies</a></li>
					<li><a href="#">Tv</a></li>
					<li><a href="#">Games</a></li>
					<li><a href="#">Collectibles</a></li>
					<li><a href="#">Videos</a></li>
					<li><a href="#">Fans</a></li>
					<li><a href="#">News</a></li>
					<li><a href="#">Shop</a></li>
				</ul>
			</nav>
		</div>
	</header>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "../assets/scss/variable.scss";

header {
	display: flex;
	background: $white;
	align-items: center;

	> div {
		width: 100%;
		display: flex;
		padding: 0.5rem;
		margin: 0 auto;
		max-width: 1280px;
		align-items: center;
		justify-content: space-between;
	}

	.logo {
		width: 64px;
		height: 64px;

		img {
			object-fit: contain;
		}
	}

	.navigation {
		display: flex;
		font-size: 1rem;
		line-height: 1.5rem;

		ul {
			display: flex;
			align-items: center;

			li {
				position: relative;
				padding: 1.5rem 0.5rem;

				a {
					color: $gray-500;
					font-weight: 600;
					text-transform: uppercase;
					transition: color 0.1s ease;

					&:hover,
					&:focus,
					&:active {
						color: $blue-500;
					}
				}

				&.active {
					a {
						color: $blue-500;
					}

					&::before {
						left: 0;
						top: 100%;
						width: 100%;
						content: "";
						height: 0.125rem;
						position: absolute;
						background: $blue-500;
					}
				}
			}
		}
	}
}
</style>
