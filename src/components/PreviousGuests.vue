<template>
	<div class="columns is-multiline">
		<div
			class="column is-12-mobile is-4-desktop"
			v-for="profile in profiles"
			:key="profile.id"
		>
			<Profile :src="profile.src" :name="profile.name" :twitter="profile.twitter"></Profile>
		</div>
	</div>
</template>

<script>
import S1guza from "@/assets/profiles/s1guza.png";
import Coolstar from "@/assets/profiles/coolstar.jpg";
import Kirb from "@/assets/profiles/kirb.jpg";
import iBSparkes from "@/assets/profiles/ibsparkes.jpg";
import Moses from "@/assets/profiles/moses.jpg";
import Micah from "@/assets/profiles/micah.jpg";
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
				},
				{
					id: 4,
					name: "iBSparkes",
					src: iBSparkes,
					twitter: "https://twitter.com/iBSparkes"
				},
				{
					id: 5,
					name: "Moses Buckwalter",
					src: Moses,
					twitter: "https://twitter.com/MosesBuckwalter"
				},
				{
					id: 6,
					name: "Micah Gomez",
					src: Micah,
					twitter: "https://twitter.com/micahpgomez"
				},
			]
		};
	}
};
</script>

<style></style>
