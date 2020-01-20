<template>
	<div class="columns is-multiline">
		<div
			class="column is-6-mobile is-4-desktop"
			v-for="profile in profiles"
			:key="profile.id"
		>
			<Profile :src="profile.src" :name="profile.name"></Profile>
		</div>
	</div>
</template>

<script>
import S1guza from "@/assets/profiles/s1guza.png";
import Coolstar from "@/assets/profiles/coolstar.jpg";
import Kirb from "@/assets/profiles/kirb.jpg";
import Profile from "@/components/Profile";

export default {
	components: {
		Profile
	},
	data() {
		return {
			profiles: [
				{
					id: 1,
					name: "S1guza",
					src: S1guza,
					twitter: "https://twitter.com/s1guza"
				},
				{
					id: 2,
					name: "Coolstar",
					src: Coolstar,
					twitter: "https://twitter.com/CStar_OW"
				},
				{
					id: 3,
					name: "Kirb",
					src: Kirb,
					twitter: "https://twitter.com/hbkirb"
				}
			]
		};
	}
};
</script>

<style></style>
