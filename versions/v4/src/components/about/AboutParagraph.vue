<template>
  <div class="about-paragraph" :class="[ isRight ? 'about-paragraph--right' : '']">
    <div class="about-paragraph__header">{{ header1 }}</div>
    <div class="about-paragraph__header about-paragraph__header--bottom">{{ header2 }}</div>
    <div class="about-paragraph__paragraph">{{ paragraph }}</div>
  </div>
</template>

<script>
export default {
  props: {
    header1: String,
    header2: String,
    paragraph: String,
    isRight: Boolean
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";

$paragraph-width: 75%;

.about-paragraph {
  margin: $spacing-section-default 0;
  width: $paragraph-width;

  &:first-child {
    margin-top: $spacing-default;
  }

  &:last-child {
    margin-bottom: $spacing-default;
  }

  &--right {
    text-align: right;
    margin-left: 100% - $paragraph-width;
  }

  &__header {
    font-size: $font-size-header-default;
    font-weight: 700;
    letter-spacing: -1px;
    padding: 0 $spacing-default;
    color: $color-green-900;

    &--bottom {
      margin-top: -$spacing-small;
      color: $color-green-700;
    }
  }

  &__paragraph {
    margin-top: $spacing-xsmall;
    text-align: left;
    background-color: $color-green-300;
    border-radius: $border-radius-default;
    padding: $spacing-small $spacing-default;
    color: $color-green-900;
  }
}
</style>