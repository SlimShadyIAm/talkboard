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
						<div class="field has-addons badge rss">
							<div class="control">
								<input
									class="input"
									type="text"
									value="Copy RSS Feed"
								/>
							</div>
							<div class="control">
								<a
									class="button is-info"
									v-clipboard:copy="message"
								>
									Copy
								</a>
							</div>
						</div>
					</div>
				</div>
				<div class="column">
					<p class="title has-text-white">Latest episodes:</p>
					<Episodes></Episodes>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
import Episodes from "@/components/Episodes";
import VueClipboard from "vue-clipboard2";
import Vue from "vue";
VueClipboard.config.autoSetContainer = true; // add this line
Vue.use(VueClipboard);

export default {
	name: "WhereToListen",
	components: {
		Episodes
	},
	data() {
		return {
			message: "https://rss.whooshkaa.com/rss/podcast/id/7841"
		};
	}
};
</script>

<style>
.where-to-listen {
	background-color: #111111;
}

.reset {
	padding-top: 30px !important;
	padding-bottom: 50px !important;
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

.rss {
	margin-top: 30px;
	background-color: #ff851b;
}

.listen-on {
	color: #fff;
	font-size: 2.5em;
	margin-right: 30px;
}
</style>
