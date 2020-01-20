<template>
    <div>
        <IntroHome></IntroHome>
        <WhereToListen></WhereToListen>
        <HomeDetails></HomeDetails>
    </div>
</template>

<script>
import IntroHome from "@/components/IntroHome";
import WhereToListen from "@/components/WhereToListen";
import HomeDetails from "@/components/HomeDetails";

export default {
    name: "Home",
    components: {
        IntroHome,
        WhereToListen,
        HomeDetails
    }
};
</script>

<style></style>
