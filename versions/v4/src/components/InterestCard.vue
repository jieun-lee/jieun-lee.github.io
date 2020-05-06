<template>
  <div class="interest-card" :class="`interest-card--${this.position}`" @click="onClick">
    <img class="interest-card__image" :src="require(`../assets/interests/${this.name}.jpg`)" />
    <div v-if="this.position === 'mid'" class="interest-card__details">
      {{ description }}
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    description: String,
    link: Object, // label, url
    position: String // left, mid, right
  },
  methods: {
    onClick() {
      if (this.position !== "mid") {
        this.$emit("interest-clicked");
      }
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";

.interest-card {
  background-color: $color-blue-lightest;
  border-radius: $border-radius-default;

  &:not(&--mid) {
    width: 250px;
    height: 250px;
    z-index: 1;
    position: absolute;
    // border: 2px solid $color-blue-base;
    box-shadow: 2px 2px 8px 0 $shadow-lighter;

    &:hover {
      width: 255px;
      height: 255px;
      cursor: pointer;
      box-shadow: 2px 2px 12px 0 $shadow-lighter;
    }
  }

  &--mid {
    width: 350px;
    height: 350px;
    box-shadow: 2px 2px 8px 0 $shadow-darker;
    z-index: 2;
  }

  &--left {
    transform: translateX(-200px);
  }

  &--right {
    transform: translateX(200px);
  }

  &__image {
    width: 100%;
    border-top-left-radius: $border-radius-default;
    border-top-right-radius: $border-radius-default;
  }

  &__details {
    // only for mid
  }
}
</style>