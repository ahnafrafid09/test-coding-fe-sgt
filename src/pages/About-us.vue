<template>
  <div>
    <AppHeader />
    <main class="main-wrapper">
      <DividerElement />
      <div class="page-section">
        <div class="scroll-sections">
          <HeroSection />
          <SectionTwo />
          <SectionThree />
          <SectionFour />
          <GallerySection />
          <SectionSix />
          <SectionSeven />
          <SectionEight />
        </div>
        <div class="footer-section">
          <AppFooter />
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import AppHeader from "@/components/AppHeader.vue";
import DividerElement from "@/components/DividerElement.vue";
import HeroSection from "@/components/HeroSection.vue";
import SectionTwo from "@/components/SectionTwo.vue";
import SectionThree from "@/components/SectionThree.vue";
import SectionFour from "@/components/SectionFour.vue";
import GallerySection from "@/components/GallerySection.vue";
import SectionSix from "@/components/SectionSix.vue";
import SectionSeven from "@/components/SectionSeven.vue";
import SectionEight from "@/components/SectionEight.vue";
import AppFooter from "@/components/AppFooter.vue";
export default {
  name: "AboutUs",
  components: {
    AppHeader,
    HeroSection,
    DividerElement,
    SectionTwo,
    SectionThree,
    SectionFour,
    GallerySection,
    SectionSix,
    SectionSeven,
    SectionEight,
    AppFooter,
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/styles/_global";
.main-wrapper {
  background-color: #ecf5ff;
  border-radius: 0.5rem;
  flex-flow: column;
  margin: 0.75rem;
  display: flex;
}

.page-section {
  z-index: 1;
}

.scroll-sections {
  z-index: 1;
  background-color: #ecf5ff;
  min-height: 100vh;
  position: relative;
}

.footer-section {
  background-color: $white-color;
  grid-template-rows: auto;
  grid-template-columns: 1fr 1fr 1fr;
  grid-auto-columns: 1fr;
  display: block;
  position: sticky;
  bottom: 0;
  z-index: -1;
}
</style>
