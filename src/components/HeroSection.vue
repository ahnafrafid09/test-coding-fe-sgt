<template>
  <div class="header">
    <div class="gradient-logo"></div>
    <div class="header-img-overlay"></div>
    <img
      src="@/assets/image/674f102013bd946767c5ec28_Trios-Brandshoot-Liike-2700px-0402282.jpg"
      alt=""
      class="img-header"
    />
    <div class="header-img-content">
      <div class="page-padding">
        <div class="img-header-title">
          <h1 class="heading-style-h1-big" ref="waveText">
            <span class="text-logo">Trios. </span>Reliable solutions for 30
            years
          </h1>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { gsap } from "gsap";

export default {
  mounted() {
    this.animateText();
  },
  methods: {
    animateText() {
      const waveText = this.$refs.waveText;
      const textContent = waveText.textContent.trim();
      const words = textContent.split(" ");
      waveText.innerHTML = "";

      words.forEach((word, index) => {
        const wordSpan = document.createElement("span");
        wordSpan.textContent = word;
        waveText.appendChild(wordSpan);

        if (word.toLowerCase() === "trios.") {
          wordSpan.style.color = "#EE667C";
        }

        gsap.fromTo(
          wordSpan,
          { opacity: 0, y: 50 },
          {
            opacity: 1,
            y: 0,
            duration: 0.4,
            delay: 0.1 + index * 0.1,
            ease: "power3.out",
            onStart: () => {
              const letters = wordSpan.textContent.split("");
              wordSpan.innerHTML = "";

              letters.forEach((letter, letterIndex) => {
                const letterSpan = document.createElement("span");
                letterSpan.textContent = letter;
                wordSpan.appendChild(letterSpan);

                gsap.fromTo(
                  letterSpan,
                  { y: -20, rotation: -5 }, // Goyang ke atas-bawah sedikit
                  {
                    y: 0,
                    rotation: 0,
                    duration: 0.2,
                    delay: letterIndex * 0.5, // Delay lebih kecil per huruf
                    ease: "back.out(1.7)", // Efek bounce untuk animasi huruf
                    onComplete: () => {
                      gsap.to(letterSpan, {
                        opacity: 1,
                        y: 0,
                        duration: 0.2,
                        ease: "power3.out",
                      });
                    },
                  }
                );
              });
            },
          }
        );

        waveText.appendChild(document.createTextNode(" "));
      });
    },
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/styles/_global";

.header {
  height: 100vh;
  position: relative;
  z-index: -1;
}

.gradient-logo {
  z-index: 3;
  background-color: #c7919100;
  background-image: radial-gradient(
    circle farthest-side at 10% -10%,
    #fff,
    #fff0 46%
  );
  position: absolute;
  inset: 0%;
}
.header-img-overlay {
  cursor: none;
  mix-blend-mode: multiply;
  background-color: #2b346799;
  width: 100%;
  height: 100%;
  position: absolute;
  inset: 0%;
}

.header-img-content {
  width: 100%;
  padding-bottom: 9.5rem;
  position: absolute;
  inset: auto 0% 0%;
}
.page-padding {
  align-self: center;
  margin-left: auto;
  margin-right: auto;
  padding-left: 7%;
  padding-right: 7%;
}

.img-header-title {
  width: 46.0625rem;
}

.heading-style-h1-big {
  color: $white-color;
  font-size: 5.5rem;
  font-weight: 500; /* Mengurangi ketebalan font */
  line-height: 1.2; /* Memberikan ruang antar baris */
  letter-spacing: 1px; /* Memberikan sedikit ruang antar huruf */
}

.img-header {
  object-fit: cover;
  width: 100%;
  height: 100%;
}
img {
  width: auto;
  max-width: 100%;
  height: auto;
  display: inline-block;
}
</style>
