<template>
  <div class="about-paragraph" :class="[ isRight ? 'about-paragraph--right' : '']">
    <div class="about-paragraph__header-wrapper">
      <span class="about-paragraph__header">{{ header1 }} </span>
      <span class="about-paragraph__header about-paragraph__header--bottom">{{ header2 }}</span>
    </div>
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
@import "@/scss/_mediaquery.scss";

$paragraph-width: 75%;

.about-paragraph {
  margin: $spacing-section-default 0;

  @include phablet-and-larger {
    &--right {
      text-align: right;
    }
  }

  @include desktop-and-larger {
    width: $paragraph-width;
    &--right {
      margin-left: 100% - $paragraph-width;
    }
  }

  &:first-child {
    margin-top: $spacing-default;
  }

  &:last-child {
    margin-bottom: $spacing-default;
  }

  &__header {
    font-size: $font-size-header-default;
    line-height: $font-size-header-default;
    font-weight: $font-weight-bold-2;
    letter-spacing: -0.5px;
    color: $color-green-900;

    @include small-phone {
      font-size: $font-size-header-small;
    }

    @include phablet-and-larger {
      &--bottom {
        color: $color-green-700;
        display: block;
      }
    }
  }

  &__header-wrapper {
    padding: 0 $spacing-default;
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