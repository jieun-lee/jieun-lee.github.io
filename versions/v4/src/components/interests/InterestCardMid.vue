<template>
  <div class="interest-card-mid">
    <img class="interest-card-mid__image" :src="require(`@/assets/interests/${this.name}.jpg`)" />
    <div class="interest-card-mid__details">
      <div class="interest-card-mid__details__text">
        <h3 class="interest-card-mid__details__text__name">{{ name }}</h3>
        <p class="interest-card-mid__details__text__description">{{ description }}</p>
      </div>
      <a
        class="interest-card-mid__details__link"
        :href="this.link.url" target="_blank"
      >
        {{ this.link.label }}
      </a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    description: String,
    link: Object, // label, url
  },
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
@import "@/scss/_mixins.scss";

$mid-card-dims: 350px;
$mid-card-margins: 0 $spacing-large;
$mid-card-bg: $color-component-bg;
$mid-card-text-min-height: 80px;
$mid-card-shadow: 2px 2px 8px 0 $color-green-900-40;
$mid-card-image-blur: 0px -16px 50px 50px $mid-card-bg;

.interest-card-mid {
  background-color: $mid-card-bg;
  border-radius: $border-radius-default;
  width: $mid-card-dims;
  height: $mid-card-dims;
  box-shadow: $mid-card-shadow;
  z-index: 2;
  overflow: hidden;

  &__image {
    border-top-left-radius: $border-radius-default;
    border-top-right-radius: $border-radius-default;
    width: $mid-card-dims;
    position: absolute;
    z-index: -1;
  }

  &__details {
    height: $mid-card-dims;
    display: flex;
    flex-direction: column;
    place-content: flex-end;

    &__text {
      min-height: $mid-card-text-min-height;
      background-color: $mid-card-bg;
      box-shadow: $mid-card-image-blur;

      &__name {
        text-transform: uppercase;
        margin: $mid-card-margins;
        font-size: $font-size-large;
        letter-spacing: 2px;
      }

      &__description {
        margin: $mid-card-margins;
        font-size: $font-size-small;
      }
    }

    &__link {
      @include button-light;
      padding: $spacing-xsmall $spacing-default;
      margin-right: $spacing-large;
      margin-bottom: $spacing-large;
      align-self: flex-end;
      text-decoration: none;
    }
  }
}
</style>