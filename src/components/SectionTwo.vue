<template>
  <div id="intro" class="section-intro background">
    <div class="container">
      <div class="space"></div>
      <div class="intro-text-grid">
        <div class="wrapper">
          <div class="dot"></div>
          <p class="text-intro is-white">
            For 30 years, our team has treated every project as if it were our
            own, with a great sense of responsibility. About the result, about
            your budget and your secrets. We realize what your company really
            needs and ensure that the solution stands like a stone.<br /><br />We
            combine experience in various sectors and craftsmanship into
            customized solutions. In this, we go further than simply executing;
            we think along and always keep your interests in mind. That is where
            our strength lies. Trust in solutions that go beyond demand.
          </p>
        </div>
      </div>
      <div class="space"></div>
    </div>
    <div class="divider-shape w-embed">
      <img src="@/assets/image/download (2).svg" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionTwo",
};
</script>

<style lang="scss" scoped>
@import "@/assets/styles/_global";

.background {
  background-color: $primary-color;
}

.intro-text-grid {
  grid-column-gap: 1rem;
  grid-row-gap: 1rem;
  grid-template-rows: auto;
  grid-template-columns: 1.25fr 1.25fr 5.75rem;
  grid-auto-columns: 1fr;
  display: grid;
}

.page-padding {
  align-self: center;
  margin-left: auto;
  margin-right: auto;
  padding-left: 7%;
  padding-right: 7%;
}

.intro-text {
  grid-column-gap: 1rem;
  grid-row-gap: 1rem;
  grid-template-rows: auto;
  grid-template-columns: 1.25fr 1.25fr 5.75rem;
  grid-auto-columns: 1fr;
  display: grid;
}

.wrapper {
  display: flex;
  position: relative;
  grid-column: 2;
}

.text-intro.is-white {
  color: $white-color;
}
.text-intro {
  text-indent: 1.5rem;
  font-size: 1.25rem;
}

.divider-shape {
  width: 100%;
  display: block;
  top: 1rem;
  //   border: 2px solid black;
  position: relative;
}
</style>
