<template>
  <div class="section" :class="'section--'+theme" :id=id>
    <div class="section__wrapper">
      <h3 class="section__title">{{ title }}</h3>
    <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    id: String,
    theme: String,
  },
  computed: {
    title() {
      return this.id.toUpperCase();
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";

.section {
  min-height: 300px;

  &--dark {
    background-color: $color-blue-light;
  }
  &--light {
    background-color: $color-blue-lighter;
  }

  &__wrapper {
    width: 100%;
    max-width: 700px;
    margin: auto;
  }

  &__title {
  color: $color-text;
  letter-spacing: 5px;
  }
}
</style>