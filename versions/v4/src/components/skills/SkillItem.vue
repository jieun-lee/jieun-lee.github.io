<template>
  <div class="skill">
    <div class="skill__label">{{ name }}</div>
    <div class="skill__bar">
      <div class="skill__bar__value">{{ level }}<span class="skill__bar__value__percent">%</span></div>
      <div
        class="skill__bar__filled"
        :class="[colored ? 'skill__bar__filled--color' : '']"
        :style="{width:level+'%'}">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    level: Number,
    categories: Array
  },
  computed: {
    colored() {
      return (this.level > 65);
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";

$skill-label-width: 120px;
$skill-bar-height: 24px;

.skill {
  display: flex;
  margin: $spacing-large;

  &__label {
    font-weight: 600;
    width: $skill-label-width;
    text-align: right;
    margin-right: $spacing-default;
  }

  &__bar {
    background-color: $color-component-bg;
    border-radius: $border-radius-default;
    height: $skill-bar-height;
    width: 100%;

    &__value {
      float: right;
      height: 100%;
      display: flex;
      align-items: center;
      padding-right: $spacing-xsmall;
      font-size: $font-size-small;
      color: $color-grey-300;

      &__percent {
        font-size: $font-size-xsmall;
      }
    }

    &__filled {
      background-color: $color-grey-300;
      border-top-left-radius: $border-radius-default;
      border-bottom-left-radius: $border-radius-default;
      height: 100%;

      &--color {
        background-color: $color-green-600;
      }
    }
  }
}
</style>