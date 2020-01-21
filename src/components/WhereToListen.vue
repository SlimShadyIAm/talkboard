<template>
    <section class="hero where-to-listen">
        <div class="hero-body reset">
            <div class="container">
                <div class="columns">
                    <div class="column is-3">
                        <!-- <p class="listen-on">Listen on:</!-->
                        <p class="title has-text-white has-text-centered">Where to listen</p>
                        <div class="badges">
                            <a href="https://open.spotify.com/show/1sCjmMpUDqnJNU54KwRf2Z">
                                <img class="badge" src="@/assets/spotify-badge.png" />
                            </a>
                            <br />
                            <a href="https://podcasts.apple.com/gb/podcast/talkboard/id1469760640">
                                <img class="badge" src="@/assets/apple-badge.png" />
                            </a>
                            <div class="badge rss">
                                <a class="button copy-text">Copy RSS Link</a>
                                <a
                                    class="button is-info copy-button"
                                    v-clipboard:copy="message"
                                >Copy</a>
                            </div>
                        </div>
                    </div>
                    <div class="column">
                        <p class="title has-text-white">Latest episodes</p>
                        <Episodes></Episodes>
                    </div>
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
    background-color: #272829;
}

.reset {
    padding-top: 30px !important;
    padding-bottom: 50px !important;
}

.badges {
    display: flex;
    justify-content: center;
    flex-direction: column;
    height: 80%;
}

.badge {
    width: 225px;
    margin: 10px;
    display: block;
    margin: 0 auto;
}

.rss {
    margin-top: 30px;
    display: inline-block;
}

.copy-text {
    border-top-right-radius: 0px;
    border-bottom-right-radius: 0px;
    width: 65%;
}

.copy-button {
    border-top-left-radius: 0px;
    border-bottom-left-radius: 0px;
    width: 35%;
}

.listen-on {
    color: #fff;
    font-size: 2.5em;
    margin-right: 30px;
}
</style>
