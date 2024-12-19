<template>
  <div class="nav">
    <div class="navbar">
      <div class="navbar-container">
        <a href="" class="navbar-logo">
          <img class="logo" src="@/assets/image/download (3).svg" alt="logo" />
        </a>
        <nav role="navigation" class="navbar_menu w-nav-menu">
          <div class="navbar-menu-links">
            <a
              v-for="(item, index) in navItems"
              :key="index"
              :href="item.link"
              class="nav-button w-inline-block"
            >
              <div class="nav-background"></div>
              <div class="nav-button-text">{{ item.text }}</div>
            </a>

            <div class="dropdown" @click.stop="toggleDropdown">
              <button class="dropbtn">
                <img
                  src="@/assets/image/6744812e2d44005ba3ac9d47_Engels.svg"
                  alt=""
                />
                <img
                  class="nav-button-text"
                  src="@/assets/image/download (5).svg"
                  alt=""
                />
              </button>
              <div
                class="dropdown-content nav-button-text"
                :class="{ show: isDropdownOpen }"
              >
                <a
                  class="text-dropdown"
                  href="#"
                  @click.prevent="changeLanguage('en')"
                  ><img
                    src="@/assets/image/674480fad4fc2c1bef58e509_Nederlands.svg"
                    alt=""
                  />Nederlands</a
                >
                <a
                  class="text-dropdown"
                  href="#"
                  @click.prevent="changeLanguage('id')"
                  ><img
                    src="@/assets/image/6744812e2d44005ba3ac9d47_Engels.svg"
                    alt=""
                  />English</a
                >
              </div>
            </div>
          </div>
        </nav>
      </div>
    </div>
  </div>
</template>

<script>
import { gsap } from "gsap";

export default {
  name: "AppHeader",
  data() {
    return {
      navItems: [
        { text: "Home", link: "/" },
        { text: "Product development", link: "/" },
        { text: "Mechanical engineering", link: "/" },
        { text: "Vacancies", link: "/" },
        { text: "About trios", link: "/" },
        { text: "Contact", link: "/" },
      ],
      isDropdownOpen: false, // Untuk melacak status dropdown
    };
  },
  methods: {
    changeLanguage(language) {
      console.log("Language changed to:", language);
      this.isDropdownOpen = false;
    },
    toggleDropdown() {
      this.isDropdownOpen = !this.isDropdownOpen;
    },
  },
  mounted() {
    const navButtons = document.querySelectorAll(".nav-button");

    navButtons.forEach((button) => {
      const background = button.querySelector(".nav-background");

      button.addEventListener("mouseenter", () => {
        gsap.to(background, {
          scaleY: 1,
          backgroundColor: "#DEE7F4",
          transformOrigin: "bottom",
          duration: 0.3,
          ease: "power1.inOut",
        });
      });

      button.addEventListener("mouseleave", () => {
        gsap.to(background, {
          scaleY: 0,
          backgroundColor: "white",
          transformOrigin: "bottom",
          duration: 0.3,
          ease: "power1.inOut",
        });
      });
    });
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/styles/_global";

.nav {
  width: 100%;
  height: 6rem;
  position: absolute;
  z-index: 103;
}

.navbar {
  background-color: #ddd0;
  width: 100%;
  height: 100%;
  position: absolute;
  inset: 0% 0% auto;
}

.navbar-container {
  justify-content: space-between;
  align-items: center;
  width: 100%;
  height: 100%;
  margin-left: auto;
  margin-right: auto;
  padding-left: 7%;
  padding-right: 7%;
  display: flex;
}

.navbar-logo {
  float: left;
  color: #333;
  text-decoration: none;
  position: relative;
}

.logo {
  color: #fff;
  justify-content: center;
  align-items: center;
  display: flex;
}

.navbar_menu {
  align-items: center;
  display: block;
  position: static;
}

.navbar-menu-links {
  grid-column-gap: 0.25rem;
  grid-row-gap: 0.25rem;
  justify-content: flex-start;
  align-items: center;
  display: flex;
}

.nav-button {
  background-color: $white-color;
  text-align: center;
  border-radius: 0.5rem;
  padding: 0.6rem 1.25rem;
  text-decoration: none;
  position: relative;
  overflow: hidden;
  display: inline-block;
  z-index: 1;
}

.nav-background {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: $white-color;
  transform-origin: bottom;
  transform: scaleY(0);
  z-index: -1;
}

.nav-button-text {
  color: $primary-color;
  font-size: 1rem;
  font-weight: 500;
}

.dropdown {
  position: relative;
  display: inline-block;
}

.dropbtn {
  background-color: $white-color;
  border: 1px #000;
  border-radius: 0.5rem;
  padding: 0.6rem 1.25rem;
  font-size: 1rem;
  color: $primary-color;
  display: flex;
  align-items: center;
  justify-items: center;
  gap: 0.5rem;
  cursor: pointer;
}
.dropdown-content {
  position: absolute;
  background-color: $white-color;
  border-radius: 0.5rem;
  min-width: 160px;
  z-index: 10;
  opacity: 0;
  top: 50px;
  left: 0px;
  visibility: hidden;
  transition: all 0.3s ease;
}

.dropdown-content a {
  color: $primary-color;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}

.dropdown-content a:hover {
  background-color: #dee7f4;
  border-radius: 0.5rem;
}

.dropdown-content.show {
  opacity: 1;
  visibility: visible;
}

.text-dropdown {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1rem;
}
</style>
