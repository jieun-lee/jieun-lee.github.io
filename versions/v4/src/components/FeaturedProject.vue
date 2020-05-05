<template>
  <div class="featured-project">
    <img class="featured-project__image" :src="require(`../assets/projects/${this.imgsrc}.jpg`)" />
    <div class="featured-project__details">
      <div class="featured-project__name">{{ name }}</div>
      <div class="featured-project__description">{{ description }}</div>
    </div>
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

.featured-project {
  display: flex;
  background-color: $color-blue-lightest;
  margin-bottom: 16px;
  border-radius: $border-radius-default;

  &__image {
    max-width: 225px;
    border-top-left-radius: $border-radius-default;
    border-bottom-left-radius: $border-radius-default;
    border-right: 2px solid $color-grey-lighter;
  }

  &__details {
    padding: 16px;
  }

  &__name {
    font-weight: 600;
    font-size: 18px;
  }

  &__description {
    font-size: 14px;
  }
}
</style>