<template>
  <div class="team">
    <div class="space"></div>
    <div class="container">
      <div class="team-title-grid">
        <div
          id="w-node-_6449322e-320e-baa7-2a78-c0f0d7197d79-d7197d76"
          class="team-text-wrapper"
        >
          <div class="dot"></div>
          <p class="text-intro is-dark">
            Our professionals. The driving force behind our solutions
          </p>
        </div>
      </div>
      <div
        id="w-node-_6449322e-320e-baa7-2a78-c0f0d7197d7d-d7197d76"
        class="spacer-large"
      ></div>
      <div class="team-wrapper w-dyn-list">
        <div role="list" class="team-grid w-dyn-items">
          <CardTeam
            v-for="(member, index) in teamMembers"
            :key="index"
            :image="member.image"
            :name="member.name"
          />
        </div>
      </div>
    </div>

    <div class="space"></div>
  </div>
</template>

<script>
import CardTeam from "./ui/CardTeam.vue";

export default {
  name: "SectionFour",
  components: { CardTeam },
  data() {
    return {
      teamMembers: [
        {
          image: require("@/assets/image/6751cb02fc6576289b79638f_Trios-Portretten-Liike-2700px-0402069.jpg"),
          name: "Ina Hulzink",
        },
        {
          image: require("@/assets/image/6751ca4967227b93a7240d78_Trios-Portretten-Liike-2700px-0402012.jpg"),
          name: "Sil Screever",
        },
        {
          image: require("@/assets/image/6751ca5cc8df56e77609770c_Trios-Portretten-Liike-2700px-0402020.jpg"),
          name: "Hefney de Haan",
        },
        {
          image: require("@/assets/image/6751ca0de85c1178d5151108_Trios-Portretten-Liike-2700px-0401979.jpg"),
          name: "Wessel Warmink",
        },
        {
          image: require("@/assets/image/6751ca6aa7388431918c69d8_Trios-Portretten-Liike-2700px-0402028.jpg"),
          name: "Max Porskamp",
        },
        {
          image: require("@/assets/image/6751c9dfe29855d6d517b6a9_Trios-Portretten-Liike-2700px-0401966.jpg"),
          name: "Hans Groothornte",
        },
        {
          image: require("@/assets/image/6751c9c788dc8ddccaa1c5ce_Trios-Portretten-Liike-2700px-0401962.jpg"),
          name: "Erik van Gaasbeek",
        },
        {
          image: require("@/assets/image/6751cac1e85c1178d515e4e5_Trios-Portretten-Liike-2700px-0402051.jpg"),
          name: "Mick Borgelink",
        },
        {
          image: require("@/assets/image/6751cb127a99cd5d470dcd09_Trios-Portretten-Liike-2700px-0402080.jpg"),
          name: "Wouter Bos",
        },
        {
          image: require("@/assets/image/6751c9fb396ee9e40cbdeb43_Trios-Portretten-Liike-2700px-0401977.jpg"),
          name: "Marc Ottenschot",
        },
        {
          image: require("@/assets/image/6751cadec8df56e7760a242f_Trios-Portretten-Liike-2700px-0402057.jpg"),
          name: "Rene Freriksen",
        },
        {
          image: require("@/assets/image/6751cab41d4b4847cf0dfda0_Trios-Portretten-Liike-2700px-0402045.jpg"),
          name: "Martijn klein Kranenbarg",
        },
        {
          image: require("@/assets/image/6751ca1d20672329a9f8586f_Trios-Portretten-Liike-2700px-0401986.jpg"),
          name: "Tom Denekamp",
        },
        {
          image: require("@/assets/image/6751ca8be85c1178d515a125_Trios-Portretten-Liike-2700px-0402037.jpg"),
          name: "Dick Boerstoel",
        },
        {
          image: require("@/assets/image/6751ca3ae42c08b52ffe781c_Trios-Portretten-Liike-2700px-0402006.jpg"),
          name: "Sjoerd van der Velde",
        },
        {
          image: require("@/assets/image/6751ca2d20672329a9f8697b_Trios-Portretten-Liike-2700px-0401997.jpg"),
          name: "Michel Lammers",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/styles/_global";
.team-title-grid {
  grid-column-gap: 1rem;
  grid-row-gap: 1rem;
  grid-template-rows: auto;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-auto-columns: 1fr;
  display: grid;
}
#w-node-_6449322e-320e-baa7-2a78-c0f0d7197d79-d7197d76 {
  grid-area: 1 / 4 / 2 / 5;
}
.team-text-wrapper {
  display: flex;
  position: relative;
}

.text-intro.is-dark {
  color: #2b3467b3;
}
.text-intro {
  text-indent: 1.5rem;
  font-size: 1.25rem;
}

.spacer-large {
  padding-top: 2.5rem;
}

.team-grid {
  grid-column-gap: 16px;
  grid-row-gap: 16px;
  grid-template-rows: auto;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-auto-columns: 1fr;
  display: grid;
}
</style>
