<template>
	<header>
		<div>
			<div class="logo">
				<a href="#">
					<img
						src="../assets/images/dc-logo.png"
						alt="dc-logo-image"
					/>
				</a>
			</div>
			<nav class="navigation">
				<ul>
					<li
						v-for="(link, index) in navigationLink"
						:key="index"
						:class="{ active: index === 0 }"
					>
						<a href="#">{{ link }}</a>
					</li>
				</ul>
			</nav>
		</div>
	</header>
</template>

<script>
export default {
	name: "Header",
	data() {
		return {
			navigationLink: [
				"Characters",
				"Comics",
				"Movies",
				"Tv",
				"Games",
				"Collectibles",
				"Videos",
				"Fans",
				"News",
				"Shop",
			],
		};
	},
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/variable.scss";

header {
	display: flex;
	background: $white;
	align-items: center;

	> div {
		@include container;

		> .logo {
			width: 64px;
			height: 64px;

			img {
				object-fit: contain;
			}
		}

		> .navigation {
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
						color: $gray-600;
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
							width: 100%;
							content: "";
							height: 0.25rem;
							position: absolute;
							background: $blue-500;
							top: calc(100% + 0.25rem);
						}
					}
				}
			}
		}
	}
}
</style>
