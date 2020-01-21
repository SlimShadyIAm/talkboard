<template>
	<!-- <div class="episode-card column is-3">
		<p class="episode-title">{{ title }}</p>
		<p class="episode-desc">
			{{
				description
					.split(" ")
					.splice(0, 15)
					.join(" ") + "..."
			}}
		</p>
	</div> -->
	<div class="card column is-3">
		<div class="card-content">
			<div class="media">
				<div class="media-content">
					<p class="title is-4 has-text-white">{{ episode.title }}</p>
					<p class="subtitle is-6 has-text-white">
						Season {{ episode.itunes.season }}, Epsiode
						{{ episode.itunes.episode }}
					</p>
				</div>
			</div>

			<div class="content has-text-white">
				{{ episode.contentSnippet }}<br />
				<time>{{ timestamp }}</time>
			</div>
		</div>
	</div>
</template>

<script>
var moment = require("moment");
export default {
	name: "Episode",
	props: ["episode"],
	data() {
		return {
			timestamp: moment(this.episode.pubDate).fromNow()
		};
	}
};
</script>

<style>
.card {
	background-color: rgb(37, 37, 37);
	margin-right: 10px;
	width: auto;
}

.episode-title {
	color: #fff;
	font-size: 22px;
	font-weight: 600;
}

.episode-desc {
	color: #fff;
}

time {
	color: rgb(175, 175, 175);
}
</style>
