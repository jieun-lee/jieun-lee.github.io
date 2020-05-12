<template>
  <div class="section" :class="'section--'+theme" :id=id>
    <div class="section__wrapper">
      <h2 class="section__title" v-if="!hideHeader">{{ title }}</h2>
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    id: String,
    theme: String,
    hideHeader: {
      type: Boolean,
      deafult: false
    }
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
@import "@/scss/_mixins.scss";

$content-area-width: 768px;

.section {
  padding: $spacing-section-small $spacing-default $spacing-section-default;

  &--dark {
    background-color: $color-green-300;
  }
  &--light {
    background-color: $color-green-200;
  }

  &__wrapper {
    width: 100%;
    max-width: $content-area-width;;
    margin: auto;
  }

  &__title {
    @include section-title;
  }
}
</style>