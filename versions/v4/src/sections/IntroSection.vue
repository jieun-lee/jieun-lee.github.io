<template>
  <div class="section intro" id="intro">
    <div class="intro__wrapper">
      <div class="intro__nametag">
        <div class="intro__nametag__name">Jieun Lee</div>
        <div class="intro__nametag__description">Software Developer based in Vancouver, BC</div>
      </div>
      <div class="intro__links">
        <a v-for="link in links" :key="link.name" :href="link.url" target="_blank">
          <img class="intro__links__icon" :src="require(`@/assets/icons/icon-${link.imgsrc}`)" />
        </a>
      </div>
    </div>
    <img class="intro__background" src="@/assets/introbg.jpg" />
  </div>
</template>

<script>
import linkData from "@/data/links.json";
export default {
  data() {
    return {
      links: linkData.links
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
@import "@/scss/_mixins.scss";
@import "@/scss/_mediaquery.scss";

$intro-section-height: 500px;
$intro-section-height-sm: 350px;
$intro-section-border: 8px solid $color-green-700;
$intro-name-letter-spacing: 0.75px;

.intro {
  height: $intro-section-height-sm;
  position: relative;
  overflow: hidden;
  background-color: $color-green-700; // when img doesn't load
  border-bottom: $intro-section-border;

  @include tablet-and-larger {
    height: $intro-section-height;
  }

  &__background {
    @include cover-with-image;
    object-position: left;
    position: absolute;
    top: 0;
    left: 0;
    filter: brightness(1.05);
  }

  &__wrapper {
    position: relative;
    z-index: 1;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    place-content: center;
    align-items: center;
  }

  &__nametag {
    background-color: $color-grey-100-75;
    text-align: center;
    padding: $spacing-section-small;
    margin: 0 $spacing-large $spacing-default;
    border-radius: $border-radius-extra;

    @include phablet-and-larger {
      padding: $spacing-section-xsmall $spacing-section-large;
    }

    &__name {
      font-family: 'Roboto Slab';
      font-weight: $font-weight-bold-title;
      font-size: $font-size-header-large;
      letter-spacing: $intro-name-letter-spacing;
      line-height: 1;
    }

    &__description {
      font-size: $font-size-large;
    }
  }

  &__links {
    &__icon {
      margin: 0 $spacing-default;
      transform: scale(0.96);

      &:hover {
        transform: scale(1);
      }
    }
  }
}
</style>