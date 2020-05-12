<template>
  <div class="interest-card-mini">
    <img class="interest-card-mini__image" :src="require(`@/assets/interests/${this.name}.jpg`)" />
    <div class="interest-card-mini__details">
      <div class="interest-card-mini__details__text">
        <h3 class="interest-card-mini__details__text__name">{{ name }}</h3>
        <p class="interest-card-mini__details__text__description">{{ description }}</p>
      </div>
      <a
        class="interest-card-mini__details__link"
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
@import "@/scss/_mediaquery.scss";

$mini-card-margins: 0 $spacing-large;
$mini-card-bg: $color-component-bg;
$mini-card-text-min-height: 80px;
$mini-card-shadow: 2px 2px 8px 0 $color-green-900-40;
$mini-card-image-blur: 0px -16px 50px 50px $mini-card-bg;
$mini-card-image-blur-sm: -10px 0px 70px 70px $mini-card-bg;
$mini-card-img-width-sm: 300px;
$mini-card-img-max-height-sm: 180px;

.interest-card-mini {
  background-color: $mini-card-bg;
  border-radius: $border-radius-default;
  box-shadow: $mini-card-shadow;
  z-index: 2;
  overflow: hidden;
  width: 45%;
  margin: 0 auto $spacing-section-xsmall;
  position: relative;

  @include small-phone {
    width: 100%;
    display: flex;
  }

  &__image {
    width: 100%;
    margin-bottom: -$spacing-section-small;
    z-index: -1;

    @include small-phone {
      width: $mini-card-img-width-sm;
      max-height: $mini-card-img-max-height-sm;
      opacity: 20%;
    }
  }

  &__details {
    display: flex;
    flex-direction: column;
    place-content: flex-end;
    margin-bottom: $spacing-section-large;
    text-align: center;
    width: 100%;

    @include small-phone {
      margin-bottom: 0;
      padding: $spacing-default;
      text-align: left;
      box-shadow: $mini-card-image-blur-sm;
    }

    &__text {
      min-height: $mini-card-text-min-height;
      background-color: $mini-card-bg;
      box-shadow: $mini-card-image-blur;

      @include small-phone {
        box-shadow: none;
        background-color: transparent;
        position: absolute;
        left: 0;
        top: 0;
      }

      &__name {
        text-transform: uppercase;
        margin: $mini-card-margins;
        font-size: $font-size-large;
        letter-spacing: 2px;

        @include small-phone {
          margin-top: $spacing-default;
        }
      }

      &__description {
        margin: $mini-card-margins;
        font-size: $font-size-small;
      }
    }

    &__link {
      @include button-light;
      padding: $spacing-xsmall $spacing-default;
      align-self: center;
      position: absolute;
      bottom: $spacing-default;
      text-decoration: none;

      @include small-phone {
        right: $spacing-default;
        font-size: $font-size-small;
      }
    }
  }
}
</style>