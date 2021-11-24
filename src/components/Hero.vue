<template>
	<div class="hero">
		<div class="image">
			<img src="../assets/images/jumbotron.jpg" alt="jumbotron" />
		</div>
	</div>
</template>

<script>
export default {
	name: "Hero",
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/variable.scss";

.hero {
	width: 100%;
	& .image {
		max-height: 320px;

		img {
			width: 100%;
			height: 100%;
			object-fit: cover;
		}
	}
}
</style>
