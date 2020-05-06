<template>
  <div class="interest-card" :class="`interest-card--${this.position}`">
    {{ name }}
    <div v-if="this.position === 'mid'" class="interest-card__details">
      {{ description }}
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    imgsrc: String,
    description: String,
    link: Object, // label, url
    position: String // left, mid, right
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";

.interest-card {
  background-color: $color-blue-lightest;
  border-radius: $border-radius-default;
  width: 200px;
  height: 200px;

  &--mid {
    width: 400px;
    height: 300px;
  }

  &--left {
    // move slightly right
  }

  &--right {
    // move slightly left
  }

  &__details {
    // only for mid
  }
}
</style>