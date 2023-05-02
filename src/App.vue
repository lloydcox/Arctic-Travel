<template>
  <HeaderMenu />
  <TopBanner />
  <KeepScrolling />
  <SelectionGallery />
  <SpeakToAgent />
  <RecommendedResorts />
  <InfoSection />
  <BookNow />
  <FooterMenu />
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import TopBanner from "./components/TopBanner.vue";
import HeaderMenu from "./components/HeaderMenu.vue";
import KeepScrolling from "./components/KeepScrolling.vue";
import SelectionGallery from "./components/SelectionGallery.vue";
import SpeakToAgent from "./components/SpeakToAgent.vue";
import RecommendedResorts from "./components/RecommendedResorts.vue";
import InfoSection from "./components/InfoSection.vue";
import BookNow from "./components/BookNow.vue";
import FooterMenu from "./components/FooterMenu.vue";

export default {
  name: "App",
  components: {
    HeaderMenu,
    TopBanner,
    KeepScrolling,
    SelectionGallery,
    SpeakToAgent,
    RecommendedResorts,
    InfoSection,
    BookNow,
    FooterMenu,
  },
};
</script>

<style lang="scss">
@import "@/assets/scss/variables.scss";
// now we set all the vars from the ArcticTravel.scss file
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

body {
  margin: 0;
}
</style>
