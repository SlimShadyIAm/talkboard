<template>
	<div class="profile-outer">
		<figure class="image is-128x128">
			<img class="is-rounded" :src="src" />
		</figure>
		<p class="caption">
			{{ name }} <a target=_blank :href="twitter"><i class="fab fa-twitter"></i></a>
		</p>
	</div>
</template>

<script>
export default {
	name: "Profile",
	props: ["src", "name", "twitter"]
};
</script>

<style scoped>
.profile-outer {
	display: flex;
	align-items: center;
	justify-content: center;
	flex-direction: column;
}

.caption {
	text-align: center;
	margin-top: 10px;
	margin-bottom: 10px;
	font-size: 20px;
	font-weight: 600;
}
</style>
