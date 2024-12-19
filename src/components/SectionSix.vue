<template>
  <div>
    <div class="container">
      <div class="space hide-mobile-potrait"></div>
      <div class="wrapper">
        <div
          id="w-node-_528c18f7-5a96-3792-d908-dcd59b45fb2a-9b45fb26"
          class="cijfers-content"
        >
          <h2 class="heading-style-h2">
            Reliability at Trios: facts that speak
          </h2>
          <div
            id="w-node-_528c18f7-5a96-3792-d908-dcd59b45fb2d-9b45fb26"
            class="spacer-small"
          ></div>
          <p class="text-size-medium">
            We focus on trust, innovation and craftsmanship. We'd love to tell
            you about that, but the facts speak for themselves.
          </p>
          <div
            id="w-node-_528c18f7-5a96-3792-d908-dcd59b45fb30-9b45fb26"
            class="spacer-large"
          ></div>
          <div class="cijfers">
            <div
              data-gsap="el.6"
              id="w-node-_528c18f7-5a96-3792-d908-dcd59b45fb32-9b45fb26"
              class="cijfer"
              style="
                opacity: 1;
                visibility: inherit;
                translate: none;
                rotate: none;
                scale: none;
                transform: translate(0px, 0px);
              "
            >
              <div
                data-gsap="txt.11"
                class="heading-style-h2"
                style="opacity: 1; visibility: inherit"
              >
                30
              </div>
              <p class="text-size-regular text-color-dark">
                Years of experience
              </p>
              <p class="text-size-regular is-cijfer">
                in precision engineering solutions.
              </p>
            </div>
            <div
              data-gsap="el.6"
              id="w-node-_528c18f7-5a96-3792-d908-dcd59b45fb39-9b45fb26"
              class="cijfer"
              style="
                opacity: 1;
                visibility: inherit;
                translate: none;
                rotate: none;
                scale: none;
                transform: translate(0px, 0px);
              "
            >
              <div
                data-gsap="txt.11"
                class="heading-style-h2"
                style="opacity: 1; visibility: inherit"
              >
                50+
              </div>
              <p class="text-size-regular text-color-dark">Projects</p>
              <p class="text-size-regular is-cijfer">in various sectors</p>
            </div>
            <div
              data-gsap="el.6"
              id="w-node-_528c18f7-5a96-3792-d908-dcd59b45fb40-9b45fb26"
              class="cijfer"
              style="
                opacity: 1;
                visibility: inherit;
                translate: none;
                rotate: none;
                scale: none;
                transform: translate(0px, 0px);
              "
            >
              <div
                data-gsap="txt.11"
                class="heading-style-h2"
                style="opacity: 1; visibility: inherit"
              >
                16
              </div>
              <p class="text-size-regular text-color-dark">
                young and experienced
              </p>
              <p class="text-size-regular is-cijfer">professionals</p>
            </div>
          </div>
        </div>
      </div>
      <div class="space"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionSix",
};
</script>

<style lang="scss" scoped>
@import "@/assets/styles/_global";

.heading-style-h2 {
  font-family: Ppneuemontreal, Arial, sans-serif;
  font-size: 3rem;
  font-weight: 500;
  line-height: 120%;
}

.wrapper {
  grid-column-gap: 1rem;
  grid-row-gap: 1rem;
  grid-template-rows: auto;
  grid-template-columns: 1.25fr 1.25fr 5.75rem;
  grid-auto-columns: 1fr;
  display: grid;
}

.spacer-small {
  width: 100%;
  padding-top: 1rem;
}
.text-size-medium {
  font-size: 1.25rem;
  text-decoration: none;
}

.spacer-large {
  padding-top: 2.5rem;
}

.cijfers {
  grid-column-gap: 8px;
  grid-row-gap: 8px;
  grid-template-rows: auto auto;
  grid-template-columns: 1fr 1fr;
  grid-auto-columns: 1fr;
  display: grid;
}

.cijfer {
  background-color: $white-color;
  border-radius: 0.5rem;
  padding: 1rem;
}

#w-node-_528c18f7-5a96-3792-d908-dcd59b45fb2a-9b45fb26 {
  grid-area: 1 / 2 / 2 / 3;
}

.text-size-regular.text-color-dark {
  color: $primary-color;
}

.text-size-regular {
  color: $primary-color;
  font-size: 1rem;
}

.text-size-regular.is-cijfer {
  color: #525b85b3;
  display: flex;
}
.text-size-regular {
  color: $primary-color;
  font-size: 1rem;
}
</style>
