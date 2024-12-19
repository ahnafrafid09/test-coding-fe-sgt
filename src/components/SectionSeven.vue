<template>
  <div class="seven-section">
    <div class="seven-padding">
      <div class="wrapper">
        <div
          id="w-node-ba16830a-fb65-ff3f-fbc5-7e328900495c-89004959"
          class="images-blokken"
        >
          <div
            id="w-node-ba16830a-fb65-ff3f-fbc5-7e328900495d-89004959"
            class="tekst-blok"
          >
            <p class="text-size-medium">
              27 vacation days, and a well-arranged pension.
            </p>
          </div>
          <div
            id="w-node-ba16830a-fb65-ff3f-fbc5-7e3289004960-89004959"
            class="tekst-blok second"
          >
            <p class="text-size-medium">Daily coffee time at 10 a.m.</p>
          </div>
          <div
            id="w-node-ba16830a-fb65-ff3f-fbc5-7e3289004963-89004959"
            class="img-blok"
          >
            <div
              id="w-node-ba16830a-fb65-ff3f-fbc5-7e3289004964-89004959"
              class="img-dot"
            ></div>
            <img
              loading="lazy"
              src="@/assets/image/674f05b080a2a1e4d9db5e64_Trios-Brandshoot-Liike-2700px-0401711.webp"
              alt=""
              class="image-vacatures"
            />
          </div>
          <div
            id="w-node-ba16830a-fb65-ff3f-fbc5-7e3289004966-89004959"
            class="img-blok"
          >
            <div
              id="w-node-ba16830a-fb65-ff3f-fbc5-7e3289004967-89004959"
              class="img-dot"
            ></div>
            <img
              loading="lazy"
              src="@/assets/image/674f101f47629be28a7a68cd_Trios-Brandshoot-Liike-2700px-0401540.jpg"
              alt=""
              class="image-vacatures"
            />
          </div>
          <div
            id="w-node-ba16830a-fb65-ff3f-fbc5-7e3289004969-89004959"
            class="img-blok hide-tablet"
          >
            <div
              id="w-node-ba16830a-fb65-ff3f-fbc5-7e328900496a-89004959"
              class="img-dot"
            ></div>
            <img
              loading="lazy"
              src="@/assets/image/674f101e2f24ec777d237fd0_Trios-Brandshoot-Liike-2700px-0401453.jpg"
              alt=""
              class="image-vacatures"
            />
          </div>
        </div>
        <div
          id="w-node-ba16830a-fb65-ff3f-fbc5-7e328900496c-89004959"
          class="vacatures-content"
        >
          <h5 class="heading-style-h5">
            Our people are our driving force. We value young talent and
            experienced professionals. We are happy to invest in that. Also
            working for a company where your passion for the profession is
            central and seen? We are always looking for more talent.
          </h5>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionSeven",
};
</script>

<style lang="scss" scoped>
@import "@/assets/styles/_global";

.seven-padding {
  align-self: center;
  margin-left: auto;
  margin-right: auto;
  padding-right: 7%;
  overflow: hidden;
}

.heading-style-h5 {
  font-family: Ppneuemontreal, Arial, sans-serif;
  font-size: 1.5rem;
  font-weight: 500;
  line-height: 140%;
}
.images-blokken {
  grid-template-rows: auto auto;
  grid-template-columns: auto auto auto;
  grid-auto-columns: 1fr;
  justify-content: end;
  width: 100%;
  display: grid;
  overflow: hidden;
}
#w-node-ba16830a-fb65-ff3f-fbc5-7e328900495d-89004959 {
  grid-area: 1 / 2 / 2 / 3;
  align-self: end;
}
#w-node-ba16830a-fb65-ff3f-fbc5-7e3289004960-89004959 {
  grid-area: 2 / 3 / 3 / 4;
  align-self: start;
}
#w-node-ba16830a-fb65-ff3f-fbc5-7e3289004963-89004959 {
  grid-area: 1 / 1 / 2 / 2;
}

#w-node-ba16830a-fb65-ff3f-fbc5-7e328900495c-89004959 {
  justify-self: end;
}
#w-node-ba16830a-fb65-ff3f-fbc5-7e3289004966-89004959 {
  grid-area: 2 / 2 / 2 / 2;
}
#w-node-ba16830a-fb65-ff3f-fbc5-7e3289004969-89004959 {
  grid-area: 1 / 3 / 2 / 4;
}
#w-node-ba16830a-fb65-ff3f-fbc5-7e328900496c-89004959 {
  align-self: end;
}
.img-blok {
  aspect-ratio: 1;
  border: 1px solid $white-color;
  width: 19rem;
  display: flex;
  position: relative;
  overflow: hidden;
}
.image-vacatures {
  object-fit: cover;
  width: 100%;
  height: 100%;
}

.vacatures-content {
  width: 100%;
  padding-left: 7.25rem;
}
.img-dot {
  background-color: $white-color;
  width: 0.7645rem;
  height: 0.7645rem;
  position: absolute;
  inset: 0% 0% auto auto;
}
.wrapper {
  grid-column-gap: 1rem;
  grid-row-gap: 1rem;
  grid-template-rows: auto;
  grid-template-columns: 1.15fr 1fr;
  grid-auto-columns: 1fr;
  display: grid;
}

.text-size-medium {
  font-size: 1.25rem;
  text-decoration: none;
}
.tekst-blok {
  width: 19rem;
  padding: 1.5rem;
}
</style>
