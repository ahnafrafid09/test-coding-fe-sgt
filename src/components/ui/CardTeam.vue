<template>
  <div role="listitem" class="team-card w-dyn-item">
    <img :src="image" :alt="name" loading="lazy" class="team-card-img" />
    <div class="team-card-info">
      <div class="spacer-medium"></div>
      <p class="text-size-medium dark">{{ name }}</p>
      <p class="text-size-medium w-dyn-bind-empty"></p>
    </div>
    <div
      id="w-node-_6449322e-320e-baa7-2a78-c0f0d7197d86-d7197d76"
      class="img-dot is-blue"
    ></div>
  </div>
</template>

<script>
export default {
  name: "CardTeam",
  props: {
    image: {
      type: String,
      required: true,
    },
    name: {
      type: String,
      required: true,
    },
  },
};
</script>
<style lang="sass" scoped>
@import "@/assets/styles/_global";

.team-card {
    background-color: $white-color;
    padding: 1.25rem;
    position: relative;
  }

  .team-card-img {
    aspect-ratio: 1;
    object-fit: cover;
    width: 100%;
  }

  .spacer-medium {
    width: 100%;
    padding-top: 2rem;
  }

  .text-size-medium.dark {
    color: $primary-color;
  }

  .text-size-medium {
    font-size: 1.25rem;
    text-decoration: none;
  }

  .text-size-medium {
    font-size: 1.25rem;
    text-decoration: none;
  }
  .w-dyn-hide,
  .w-dyn-bind-empty,
  .w-condition-invisible {
    display: none !important;
  }

  .spacer-medium {
    width: 100%;
    padding-top: 2rem;
  }

  .img-dot.is-blue {
    background-color: $secondary-color;
  }

  .img-dot {
    background-color: $white-color;
    width: 0.7645rem;
    height: 0.7645rem;
    position: absolute;
    inset: 0% 0% auto auto;
  }
</style>
