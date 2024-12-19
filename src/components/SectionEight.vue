<template>
  <div class="container">
    <div class="space"></div>
    <h3 class="heading-style-h6">Vacancies</h3>
    <div class="spacer-small"></div>
    <section
      id="w-node-ba16830a-fb65-ff3f-fbc5-7e3289004970-89004959"
      class="vacatures w-dyn-list"
    >
      <div role="list" class="vacatures-grid w-dyn-items">
        <div
          data-w-id="ba16830a-fb65-ff3f-fbc5-7e3289004972"
          role="listitem"
          class="vacature-card w-dyn-item"
        >
          <a
            href="/en/vacatures/toolmaker-with-cnc-experience"
            class="vacature-link w-inline-block"
          ></a>
          <div class="vacatures-card-wrapper">
            <p class="text-size-large text-color-dark">
              Toolmaker with CNC experience
            </p>
            <div class="spacer-xsmall"></div>
            <p class="text-size-medium">
              Do you have an eye for detail, problem solving skills and, as a
              real professional, are you always looking for quality? This
              toolmaker/instrument maker vacancy is for you.
            </p>
            <div class="spacer-small"></div>
            <div class="vacatures-card-details">
              <div class="vacature-detail-item">
                <div class="vacature-dot"></div>
                <p class="text-size-medium dark">Neede</p>
              </div>
              <div class="vacature-detail-item">
                <div class="vacature-dot"></div>
                <p class="text-size-medium dark">Full-Time</p>
              </div>
              <div class="vacature-detail-item">
                <div class="vacature-dot"></div>
                <p class="text-size-medium dark">MBO</p>
              </div>
            </div>
          </div>
          <div class="overlay-vacature-card" style="height: 0%"></div>
          <div
            id="w-node-ba16830a-fb65-ff3f-fbc5-7e3289004984-89004959"
            class="img-dot is-blue"
          ></div>
        </div>
        <div
          data-w-id="ba16830a-fb65-ff3f-fbc5-7e3289004972"
          role="listitem"
          class="vacature-card w-dyn-item"
        >
          <a
            href="/en/vacatures/office-environment-cleaner"
            class="vacature-link w-inline-block"
          ></a>
          <div class="vacatures-card-wrapper">
            <p class="text-size-large text-color-dark">
              Office environment cleaner
            </p>
            <div class="spacer-xsmall"></div>
            <p class="text-size-medium">
              Will you keep our pleasant working environment clean? Then you'll
              never work alone! This is the job for you.
            </p>
            <div class="spacer-small"></div>
            <div class="vacatures-card-details">
              <div class="vacature-detail-item">
                <div class="vacature-dot"></div>
                <p class="text-size-medium dark">Neede</p>
              </div>
              <div class="vacature-detail-item">
                <div class="vacature-dot"></div>
                <p class="text-size-medium dark">18/24 hours a month</p>
              </div>
              <div class="vacature-detail-item">
                <div class="vacature-dot"></div>
                <p class="text-size-medium dark">No training required</p>
              </div>
            </div>
          </div>
          <div class="overlay-vacature-card" style="height: 0%"></div>
          <div
            id="w-node-ba16830a-fb65-ff3f-fbc5-7e3289004984-89004959"
            class="img-dot is-blue"
          ></div>
        </div>
      </div>
    </section>
    <div class="spacer-huge"></div>
  </div>
</template>

<script>
export default {
  name: "SectionEight",
};
</script>

<style lang="scss" scoped>
@import "@/assets/styles/_global";

.heading-style-h6 {
  font-family: Ppneuemontreal, Arial, sans-serif;
  font-size: 1.25rem;
  font-weight: 500;
  line-height: 140%;
}

.spacer-small {
  width: 100%;
  padding-top: 1rem;
}

.vacatures-grid {
  grid-column-gap: 16px;
  grid-row-gap: 16px;
  grid-template-rows: auto;
  grid-template-columns: 1fr 1fr;
  grid-auto-columns: 1fr;
  display: grid;
}

.vacature-dot {
  background-color: $decoration-color;
  width: 0.375rem;
  height: 0.375rem;
}

.vacature-detail-item {
  grid-column-gap: 0.75rem;
  grid-row-gap: 0.75rem;
  justify-content: flex-start;
  align-items: center;
  display: flex;
}

.vacature-card {
  background-color: $white-color;
  padding: 2rem;
  position: relative;
}

.vacature-link {
  z-index: 2;
  position: absolute;
  inset: 0%;
}

.w-inline-block {
  max-width: 100%;
  display: inline-block;
}
.vacatures-card-wrapper {
  z-index: 1;
  position: relative;
}

.text-size-large.text-color-dark {
  color: $primary-color;
}
.text-size-large {
  font-size: 1.5rem;
}

.spacer-xsmall {
  width: 100%;
  padding-top: 0.5rem;
}
.text-size-medium {
  font-size: 1.25rem;
  text-decoration: none;
}

.vacatures-card-details {
  grid-column-gap: 1.5rem;
  grid-row-gap: 1.5rem;
  justify-content: flex-start;
  align-items: center;
  display: flex;
}
.overlay-vacature-card {
  background-color: #dee7f4;
  position: absolute;
  inset: auto 0% 0%;
}
.img-dot {
  background-color: $white-color;
  width: 0.7645rem;
  height: 0.7645rem;
  position: absolute;
  inset: 0% 0% auto auto;
}
.img-dot.is-blue {
  background-color: $secondary-color;
}
.spacer-huge {
  width: 100%;
  padding-top: 6rem;
}
</style>
