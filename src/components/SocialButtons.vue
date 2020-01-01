<template>
	<div class="social-outer">
		<a href="" class="button twitter">Twitter</a>
		<a href="" class="button discord">Discord</a>
		<a href="" class="button email">Email</a>
	</div>
</template>

<script>
export default {
	name: "SocialButtons"
};
</script>

<style>
.social-outer {
	display: flex;
	align-items: center;
	justify-content: center;
	width: 100%;
}

.button {
	margin: 5px;
	border: none;
	color: #fff;
	width: 33%;
}

.twitter {
	background-color: rgb(0, 162, 255);
}

.discord {
	background-color: #7289da;
}

.email {
	background-color: #e63b3b;
}
</style>
