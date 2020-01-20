<template>
	<section class="hero where-to-listen">
		<div class="hero-body reset">
			<div class="columns">
				<div class="column is-3">
					<!-- <p class="listen-on">Listen on:</!-->

					<div class="badges">
						<img
							class="badge"
							src="@/assets/spotify-badge.png"
						/><br />
						<img class="badge" src="@/assets/apple-badge.png" />
					</div>
				</div>
				<div class="column">
					<!-- <p class="title has-text-white">Latest episodes:</p> -->
					<Episodes></Episodes>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
import Episodes from "@/components/Episodes";

export default {
	name: "WhereToListen",
	components: {
		Episodes
	}
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

.badges {
	display: flex;
	height: 100%;
	justify-content: center;
	flex-direction: column;
}

.badge {
	width: 225px;
	margin: 10px;
	display: block;
	margin: 0 auto;
}

.listen-on {
	color: #fff;
	font-size: 2.5em;
	margin-right: 30px;
}
</style>
