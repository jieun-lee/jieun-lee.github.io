<template>
  <div class="featured-project">
    <img class="featured-project__image" :src="require(`../assets/projects/${this.imgsrc}.jpg`)" />
    <div class="featured-project__name">{{ name }}</div>
    <div class="featured-project__description">{{ description }}</div>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    imgsrc: String,
    skills: Array,
    description: String,
    github: String,
    playlink: String
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
@import "@/scss/_mixins.scss";

.featured-project {
  @include project-card;

  &__image {
    width: 100%;
    border-radius: 4px;
    box-shadow: 0px 0 4px 1px rgba(1, 0, 0, 0.1);
  }

  &__name {
    font-weight: 600;
    font-size: 16px;
  }

  &__description {
    font-size: 14px;
  }
}
</style>