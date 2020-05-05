<template>
  <div class="skill">
    <div class="skill__label">{{ name }}</div>
    <div class="skill__bar">
      <div class="skill__bar__value">{{ level+"%" }}</div>
      <div class="skill__bar__filled" :style="{width:level+'%'}"></div>
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
      return (this.level > 50);
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
$bar-border-radius: 8px;

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
    background-color: $color-grey-lightest;
    border-radius: $bar-border-radius;
    height: 24px;
    width: 100%;

    &__value {
      float: right;
      height: 100%;
      padding: 2.5px 6px;
      font-size: 14px;
      color: $color-grey-light;
    }

    &__filled {
      background-color: $color-blue-base;
      border-top-left-radius: $bar-border-radius;
      border-bottom-left-radius: $bar-border-radius;
      height: 100%;
    }
  }
}
</style>