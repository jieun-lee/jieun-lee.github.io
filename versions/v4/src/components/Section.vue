<template>
  <div class="section" :class="'section--'+theme" :id=id>
    <div class="section__wrapper">
      <h2 class="section__title">{{ title }}</h2>
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
  padding: 24px 12px;

  &--dark {
    background-color: $color-yellow-200;
  }
  &--light {
    background-color: $color-yellow-300;
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
  margin-top: 0px;
  margin-bottom: 20px;
  }
}
</style>