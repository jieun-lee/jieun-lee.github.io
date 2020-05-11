<template>
  <div class="section intro" id="intro">
    <div class="intro__wrapper">
      Intro Section
    </div>
    <img class="intro__background" src="@/assets/introbg.jpg" />
  </div>
</template>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
.intro {
  height: 500px;
  position: relative;
  overflow: hidden;
  background-color: $color-green-300; // when img doesn't load
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
  }
}
</style>