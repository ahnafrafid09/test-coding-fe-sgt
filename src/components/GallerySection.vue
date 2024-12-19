<template>
  <div class="gallery-component">
    <div class="horizontal-scroll-wrapper">
      <div class="gallery_horizontal-scroll-content" ref="galleryContent">
        <a
          href="#"
          id="w-node-_0d379595-9133-ab94-32b3-b2ce89cd23c6-89cd23c2"
          class="gallery_lightbox-link w-inline-block w-lightbox"
          aria-label="open lightbox"
          aria-haspopup="dialog"
          ><div class="gallery_image-qoute">
            <div class="gallery_qoute">
              <h5 class="heading-style-h5 text-color-secondary align-center">
                Trios is strong in conceptual thinking; dividing a big problem
                into bite-sized problems and merging the sum of the small
                problems into a working whole.<br /><br />De oplossingen zijn
                verrassend en altijd goed doordacht. Ideeën en concepten worden
                intern besproken met meerdere disciplines voordat ze aan de
                klant worden gepresenteerd.<br /><br />Tijdens de ontwikkeling
                van transportoplossingen wordt uitgebreid gerekend en
                gesimuleerd. Dit proces geeft veel vertrouwen in de
                uiteindelijke resultaten.
              </h5>
              <div class="spacer-medium"></div>
              <p class="text-size-medium text-color-white align-center">René</p>
            </div>
          </div>
        </a>
        <a
          href="#"
          class="gallery_lightbox-link w-inline-block w-lightbox"
          aria-label="open lightbox"
          aria-haspopup="dialog"
          ><div class="gallery_image-wrapper">
            <img
              loading="lazy"
              src="https://cdn.prod.website-files.com/672cccfa55dcaee79acf45cf/674f1021ce2fff6650f6b3ab_Trios-Brandshoot-Liike-2700px-0402377.jpg"
              alt=""
              class="gallery_image"
            />
          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import gsap from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);

export default {
  name: "GallerySection",
  mounted() {
    const galleryContent = this.$refs.galleryContent;
    gsap.to(galleryContent, {
      xPercent: -100 * (galleryContent.children.length - 1), // Mengatur scroll agar konten bisa digulirkan secara penuh
      ease: "none",
      scrollTrigger: {
        trigger: this.$el, // Memicu scroll pada elemen ini
        start: "top top", // Mulai saat halaman pertama kali di-scroll
        end: "bottom bottom", // Scroll berhenti di bagian bawah
        scrub: true, // Sinkronisasi scroll dengan animasi
        pin: true, // Pin konten selama scroll
        anticipatePin: 1, // Memberikan sedikit kelonggaran saat pin
      },
    });
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/styles/_global";

.gallery-component {
  height: 300vh;
}

.horizontal-scroll-wrapper {
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  width: 100vw;
  max-width: 100%;
  height: 100vh;
  padding-left: 7%;
  padding-right: 7%;
  display: flex;
  position: sticky;
  top: 0;
  overflow: hidden;
}
.gallery_horizontal-scroll-content {
  grid-column-gap: 2rem;
  align-items: center;
  width: 400vh;
  display: flex;
}

.gallery_lightbox-link {
  text-decoration: none;
}

.w-inline-block {
  max-width: 100%;
  display: inline-block;
}

.gallery_image {
  object-fit: cover;
  width: 80vw;
  height: 80vh;
}
.gallery_image-qoute {
  background-color: $decoration-color;
  width: 100%;
  max-width: 100%;
  height: 100%;
  text-decoration: none;
  position: relative;
  overflow: hidden;
}
.gallery_qoute {
  flex-flow: column;
  justify-content: center;
  align-items: center;
  width: 80vw;
  height: 80vh;
  padding-left: 30rem;
  padding-right: 30rem;
  text-decoration: none;
  display: flex;
}

.gallery_lightbox-link {
  text-decoration: none;
}

.w-inline-block {
  max-width: 100%;
  display: inline-block;
}

.gallery_image-wrapper {
  width: 100%;
  max-width: 100%;
  height: 100%;
  position: relative;
  overflow: hidden;
}

.align-center {
  margin-left: auto;
  margin-right: auto;
}
.heading-style-h5.text-color-secondary.align-center {
  text-align: center;
}
.heading-style-h5 {
  font-family: Ppneuemontreal, Arial, sans-serif;
  font-size: 1.5rem;
  font-weight: 500;
  line-height: 140%;
}
.text-size-medium {
  font-size: 1.25rem;
  text-decoration: none;
}
.text-color-secondary {
  color: $secondary-color;
}

.spacer-medium {
  width: 100%;
  padding-top: 2rem;
}

.text-size-medium.text-color-white {
  color: $secondary-color;
}
</style>
