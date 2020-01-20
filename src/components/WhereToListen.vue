<template>
	<section class="hero where-to-listen">
		<div class="hero-body reset">
			<div class="flex-container">
				<!-- <p class="listen-on">Listen on:</!-->

				<img class="badge" src="@/assets/spotify-badge.png" />
				<img class="badge" src="@/assets/apple-badge.png" />
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: "WhereToListen"
};
</script>

<style>
.where-to-listen {
	background-color: #111111;
}

.reset {
	padding-top: 30px !important;
	padding-bottom: 30px !important;
}

.badge {
	height: 70px;
	margin: 10px;
}

.listen-on {
	color: #fff;
	font-size: 2.5em;
	margin-right: 30px;
}
</style>
