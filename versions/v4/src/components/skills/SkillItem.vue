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
@import "@/scss/_mediaquery.scss";

$skill-label-width: 120px;
$skill-bar-height-small: 24px;
$skill-bar-height: 26px;

.skill {
  display: flex;
  margin: $spacing-default;

  @include tablet-and-larger {
    margin: $spacing-large;
  }

  @include small-phone {
    flex-direction: column;
  }

  &__label {
    font-weight: 600;
    width: $skill-label-width;
    text-align: right;
    margin-right: $spacing-default;
    font-size: $font-size-small;
    align-self: center;

    @include tablet-and-larger {
      font-size: $font-size-default;
    }

    @include small-phone {
      margin: 0;
      width: 100%;
      text-align: left;
    }
  }

  &__bar {
    background-color: $color-component-bg;
    border-radius: $border-radius-default;
    height: $skill-bar-height-small;
    width: 100%;

    @include phablet-and-larger {
      height: $skill-bar-height;
    }

    &__value {
      float: left;
      height: 100%;
      display: flex;
      align-items: center;
      padding: 0 $spacing-small;
      font-size: $font-size-small;
      color: $color-grey-100;

      &__percent {
        font-size: $font-size-xsmall;
      }

      @include phablet-and-larger {
        float: right;
        color: $color-grey-300;
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