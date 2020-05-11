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

.skill {
  display: flex;
  margin: 16px;

  &__label {
    font-weight: 600;
    width: 120px;
    text-align: right;
    margin-right: 12px;
  }

  &__bar {
    background-color: $color-component-bg;
    border-radius: $border-radius-default;
    height: 24px;
    width: 100%;

    &__value {
      float: right;
      height: 100%;
      padding: 2.5px 6px;
      font-size: 14px;
      color: $color-grey-300;

      &__percent {
        font-size:12px;
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