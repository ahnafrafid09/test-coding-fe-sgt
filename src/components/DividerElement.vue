<template>
  <div class="divider">
    <div class="divider top hide-tablet"></div>
    <div class="divider hide-tablet"></div>

    <div
      id="discover-us"
      :style="{
        opacity: opacityValue,
        transform: `translateY(${translateYValue}px)`,
      }"
      class="scrolldown-sticky hide-tablet"
    >
      <div class="corner-shape left-corner">
        <img src="@/assets/image/download (11).svg" alt="Left corner shape" />
      </div>
      <div class="corner-shape left-corner _2">
        <img src="@/assets/image/download (11).svg" alt="Left corner shape" />
      </div>

      <a href="#" class="scrolldown-sticky-wrapper">
        <p class="text-size-regular">Discover us!</p>
        <div ref="arrowLeft" class="icon-1x1-medium w-embed">
          <img src="@/assets/image/download (5).svg" alt="arrow" />
        </div>
      </a>
    </div>

    <a href="/" class="contact-sticky w-inline-block">
      <div class="corner-shape right-corner w-embed">
        <img src="@/assets/image/download (10).svg" alt="Right corner shape" />
      </div>
      <div class="contact-sticky-wrapper">
        <button
          class="button-block-17"
          @mouseover="onHoverGiveUsProblem"
          @mouseleave="onLeaveGiveUsProblem"
        >
          <div class="button-icon-wrap-17 is-left" ref="leftArrow">
            <img src="@/assets/image/download (9).svg" alt="Icon Left" />
          </div>
          <div class="button-text-17">
            Give us a problem.<span class="text-span-3"
              >We find the solution</span
            >
          </div>
          <div class="button-icon-wrap-17 is-right" ref="rightArrow">
            <img src="@/assets/image/download (9).svg" alt="Icon Right" />
          </div>
        </button>
        <div class="contact-sticky-images">
          <img
            src="@/assets/image/674f0c34664f9125f63f70d2_sticky-contact-portret-1.png"
            alt="Contact Image 1"
            class="sticky-contact-img"
          />
          <img
            src="@/assets/image/674f0c34664f9125f63f70d2_sticky-contact-portret-1.png"
            alt="Contact Image 2"
            class="sticky-contact-img second"
          />
        </div>
      </div>
    </a>

    <div class="corner-shape left-corner-top w-embed">
      <img src="@/assets/image/download (13).svg" alt="Top Left Shape" />
    </div>
    <div class="corner-shape right-corner-top w-embed">
      <img src="@/assets/image/download (12).svg" alt="Top Right Shape" />
    </div>
  </div>
</template>

<script>
import gsap from "gsap";

export default {
  name: "DividerElement",
  data() {
    return {
      opacityValue: 1,
      translateYValue: 0,
    };
  },
  methods: {
    onHoverGiveUsProblem() {
      gsap.to(this.$refs.rightArrow, {
        x: 20,
        duration: 0.3,
        ease: "power1.out",
      });

      gsap.fromTo(
        this.$refs.leftArrow,
        {
          opacity: 0,
          x: -30,
        },
        {
          opacity: 1,
          x: 0,
          duration: 0.3,
          ease: "power1.out",
        }
      );
    },

    onLeaveGiveUsProblem() {
      gsap.to(this.$refs.rightArrow, {
        x: 0,
        duration: 0.3,
        ease: "power1.out",
      });

      gsap.to(this.$refs.leftArrow, {
        opacity: 0,
        x: -30,
        duration: 0.3,
        ease: "power1.out",
      });
    },
    checkScrollPosition() {
      const introSection = document.getElementById("intro");
      const rect = introSection.getBoundingClientRect();

      // Hitung jarak dari atas viewport ke elemen intro
      const scrollTop = rect.top;

      // Maksimal offset untuk animasi
      const maxOffset = window.innerHeight * 0.05;

      // Menghitung nilai opacity dan translateY secara proporsional
      if (scrollTop < maxOffset) {
        const progress = scrollTop / maxOffset; // Progres dari 0 ke 1
        this.opacityValue = progress; // Ubah opacity sesuai progres
        this.translateYValue = (1 - progress) * 20; // Geser ke bawah
      } else {
        this.opacityValue = 1; // Opacity penuh
        this.translateYValue = 0; // Posisi awal
      }
    },
  },
  mounted() {
    window.addEventListener("scroll", this.checkScrollPosition);
    this.checkScrollPosition();
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.checkScrollPosition);
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/styles/_global";

.corner-shape.right-corner-top {
  position: fixed;
  inset: 0.75rem 0.75rem auto auto;
}

.corner-shape.left-corner-top {
  position: fixed;
  top: 0.75rem;
  left: 0.75rem;
}

.corner-shape.right-corner.default {
  bottom: 0.75rem;
}

.corner-shape.left-corner.default {
  bottom: 0.75rem;
}

.button-icon-wrap-17.is-left {
  color: $decoration-color;
  opacity: 0;
}
.divider {
  z-index: 100;
  background-color: $white-color;
  width: 100%;
  height: 0.75rem;
  position: fixed;
  inset: auto 0% 0%;
}

.scrolldown-sticky {
  z-index: 101;
  background-color: $white-color;
  border-radius: 0.5rem;
  position: fixed;
  inset: auto auto 0% 0%;
}

.corner-shape.left-corner {
  position: fixed;
  inset: auto auto 3rem 0.75rem;
}

.corner-shape {
  z-index: 8;
  display: flex;
}

.scrolldown-sticky-wrapper {
  grid-column-gap: 0.2rem;
  grid-row-gap: 0.2rem;
  border-radius: 0.5rem;
  grid-template-rows: auto;
  grid-template-columns: auto 1fr;
  grid-auto-columns: 1fr;
  justify-content: flex-start;
  align-items: center;
  padding: 0.5rem 1.25rem;
  text-decoration: none;
  display: grid;
}

.text-size-regular {
  color: $primary-color;
  font-size: 1rem;
}

.icon-1x1-medium {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 2rem;
  height: 2rem;
}

.contact-sticky {
  z-index: 101;
  background-color: $white-color;
  border-radius: 0.5rem;
  text-decoration: none;
  position: fixed;
  inset: auto 0% 0% auto;
}

.w-inline-block {
  max-width: 100%;
  display: inline-block;
}

// Right corner contact button
.corner-shape.right-corner {
  display: flex;
  position: fixed;
  inset: auto 0.75rem 3.5rem auto;
  right: 0;
}

.left-corner {
  left: 0;
  opacity: 0;
}

.corner-shape.right-corner.contact {
  bottom: 0.75rem;
  right: 32.84rem;
}

.contact-sticky-wrapper {
  grid-column-gap: 1rem;
  grid-row-gap: 1rem;
  border-radius: 0.5rem;
  grid-template-rows: auto;
  grid-template-columns: auto auto;
  grid-auto-columns: 1fr;
  justify-content: flex-start;
  align-items: center;
  padding: 0.5rem 1.25rem;
  display: grid;
}

// Button and icon wrapping
.button-block-17 {
  grid-column-gap: 0.5rem;
  grid-row-gap: 0.5rem;
  color: #f0f0f0;
  background-color: #f0f0f000;
  display: flex;
  position: relative;
  overflow: hidden;
}

.button-icon-wrap-17 {
  z-index: 1;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  display: flex;
  position: relative;
}

.button-text-17 {
  z-index: 1;
  color: #878787;
  font-size: 1rem;
  font-weight: 500;
  display: flex;
}

.text-span-3 {
  color: $primary-color;
  padding-left: 0.5rem;
}

// Sticky images
.contact-sticky-images {
  display: flex;
}

.sticky-contact-img {
  border: 2px solid #ecf5ff;
  border-radius: 40rem;
  width: 2.5rem;
  height: 2.5rem;
  box-shadow: 0 2px 5px #0003;
}
</style>
