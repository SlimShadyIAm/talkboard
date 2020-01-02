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
                            />
                        </div>
                        <div class="text-container">
                            <p class="title">23 Aaron's Flagship Podcast</p>
                            <p class="subtitle" lang="en">
                                Candid, in-depth discussions with some of the
                                iOS jailbreaking scenes leading developers
                            </p>
                            <SocialButtons></SocialButtons>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <WhereToListen></WhereToListen>
    </div>
</template>

<script>
import Navbar from "@/components/Navbar";
import WhereToListen from "@/components/WhereToListen";
import SocialButtons from "@/components/SocialButtons";
export default {
    name: "IntroHome",
    components: {
        Navbar,
        SocialButtons,
        WhereToListen
    }
};
</script>

<style>
.purple-gradient {
    background: #8432b4;
    /* background: linear-gradient(180deg, #9f3ada 10%, #111111 100%); */
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
    padding-top: 80px !important;
    padding-bottom: 150px !important;
}

.img-container {
    flex-grow: 0.5;
    display: flex;
    justify-content: center;
}

.img-container img {
    border-radius: 20px;
    box-shadow: 1em 1em 3em 0.5em rgb(19, 18, 18);
    width: 300px;
    height: 300px;
}

@media (max-width: 768px) {
    .hero-body {
        padding-top: 0px !important;
        padding-bottom: 50px !important;
    }
    .flex-container {
        flex-direction: column;
    }
    .img-container img {
        width: 200px;
        height: 200px;
    }
}

.text-container {
    flex-grow: 1;
    flex-basis: 200px;
    display: flex;
    justify-content: center;
    flex-direction: column;
}

.text-container p {
    color: #fff;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
        Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
</style>
