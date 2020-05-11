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
</script>>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
.intro {
  height: 500px;
  position: relative;
  overflow: hidden;
  background-color: $color-green-700; // when img doesn't load
  border-bottom: 8px solid $color-green-700;

  &__background {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: left;
    position: absolute;
    top: 0;
    left: 0;
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
    padding: 24px 64px;
    margin: 12px;
    border-radius: $border-radius-extra;

    &__name {
      font-size: 40px;
      font-weight: 900;
    }

    &__description {
      font-size: 18px;
      font-weight: 500;
    }
  }

  &__links {
    &__icon {
      margin: 0 12px;
      transform: scale(0.96);

      &:hover {
        transform: scale(1);
      }
    }
  }
}
</style>