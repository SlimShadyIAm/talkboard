<template>
	<div>
		<section class="hero purple-gradient is-large">
			<div class="hero-head">
				<Navbar></Navbar>
			</div>
			<div class="hero-body">
				<div class="container">
					<div class="flex-container">
						<div class="img-container">
							<img
								src="https://is3-ssl.mzstatic.com/image/thumb/Music113/v4/ef/41/ea/ef41eadf-0200-6bcd-999b-7c8ac78d298c/source/600x600bb.jpg"
								width="300"
								height="300"
							/>
						</div>
						<div class="text-container">
							<p class="title">Hey</p>
							<p class="subtitle">Yo</p>
						</div>
					</div>
				</div>
			</div>
		</section>
	</div>
</template>

<script>
import Navbar from "@/components/Navbar";
export default {
	name: "IntroHome",
	components: {
		Navbar
	}
};
</script>

<style>
.purple-gradient {
	background: rgb(136, 46, 191);
	background: linear-gradient(
		180deg,
		rgba(136, 46, 191, 1) 0%,
		rgba(0, 0, 0, 1) 170%
	);
	/* box-shadow: inset 0em 0em 5em 0em rgb(49, 49, 49); */
}
.flex-container {
	display: flex;
	align-items: center;
	justify-content: center;
	flex-direction: row;
	width: 100%;
}
.hero-body {
	padding-top: 100px !important;
	padding-bottom: 100px !important;
}

.img-container {
	flex-grow: 1;
	display: flex;
	justify-content: center;
}

.img-container img {
	border-radius: 20px;
	box-shadow: 1em 1em 3em #000;
}

.text-container {
	flex-grow: 1.5;
}
.text-container p {
	color: #fff;
}
</style>
