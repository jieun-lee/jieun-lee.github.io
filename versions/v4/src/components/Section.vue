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

.section {
  padding: 24px 12px 48px;

  &--dark {
    background-color: $color-green-300;
  }
  &--light {
    background-color: $color-green-200;
  }

  &__wrapper {
    width: 100%;
    max-width: 768px;
    margin: auto;
  }

  &__title {
  color: $color-grey-900;
  letter-spacing: 5px;
  text-align: center;
  margin-top: 4px;
  margin-bottom: 24px;
  }
}
</style>