<template>
  <div
    class="interest-card-sub"
    :style="{ transform: this.transformValue }"
    @click="onClick"
  >
    <img class="interest-card-sub__image" :src="require(`../assets/interests/${this.name}.jpg`)" />
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    position: String // left || right
  },
  data() {
    return {
      transformValue: (this.position === "left") ? "translateX(-200px)" : "translateX(200px)"
    }
  },
  methods: {
    onClick() {
      if (this.position !== "mid") {
        this.$emit("interest-clicked");
      }
    }
  },
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";

$small-card-dims: 250px;
$small-card-hover-dims: 255px;

.interest-card-sub {
  background-color: $color-yellow-100;
  border-radius: $border-radius-default;
  width: $small-card-dims;
  height: $small-card-dims;
  z-index: 1;
  position: absolute;
  box-shadow: 2px 2px 8px 0 $shadow-lighter;
  overflow: hidden;

  &:hover {
    width: $small-card-hover-dims;
    height: $small-card-hover-dims;
    cursor: pointer;
    box-shadow: 2px 2px 12px 0 $shadow-lighter;
  }

  &__image {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: $border-radius-default;
    filter: blur(1px);
    -webkit-filter: blur(1px);
    opacity: 75%;
  }
}
</style>