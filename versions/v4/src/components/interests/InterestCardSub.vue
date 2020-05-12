<template>
  <div
    class="interest-card-sub"
    :style="{ transform: this.transformValue }"
    @click="onClick"
  >
    <img class="interest-card-sub__image" :src="require(`@/assets/interests/${this.name}.jpg`)" />
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
      transformAmount: "200px"
    }
  },
  methods: {
    onClick() {
      if (this.position !== "mid") {
        this.$emit("interest-clicked");
      }
    }
  },
  computed: {
    transformValue() {
      if (this.position === "left") {
        return "translateX(-" + this.transformAmount + ")";
      } else {
        return "translateX(" + this.transformAmount + ")";
      }
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
@import "@/scss/_mixins.scss";

$small-card-dims: 250px;
$small-card-hover-dims: 255px;
$small-card-shadow: 2px 2px 8px 0 $color-green-700-25;
$small-card-shadow-hover: 2px 2px 12px 0 $color-green-700-25;
$small-card-img-filter: brightness(0.5) blur(1px);

.interest-card-sub {
  border-radius: $border-radius-default;
  width: $small-card-dims;
  height: $small-card-dims;
  z-index: 1;
  position: absolute;
  box-shadow: $small-card-shadow;
  overflow: hidden;

  &:hover {
    width: $small-card-hover-dims;
    height: $small-card-hover-dims;
    box-shadow: $small-card-shadow-hover;
    cursor: pointer;
  }

  &__image {
    @include cover-with-image;
    border-radius: $border-radius-default;
    filter: $small-card-img-filter;
    -webkit-filter: $small-card-img-filter;
    opacity: 75%;
  }
}
</style>