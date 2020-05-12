<template>
<!-- Copied from V3 -->
  <div class="nav">
    <a href="#" class="nav__link">TOP</a> ||
    <a href="#about" class="nav__link">About</a> |
    <a href="#skills" class="nav__link">Skills</a> |
    <a href="#projects" class="nav__link">Projects</a> |
    <a href="#interests" class="nav__link">Interests</a> |
    <a href="#more" class="nav__link">More</a>
  </div>
</template>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
.nav {
    position: fixed;
    z-index: 5;
    top: 0;
    right: 0;
    padding: 4px 12px;
    background-color: $color-grey-900;
    border-bottom-left-radius: $border-radius-default;
    color: $color-grey-100;
    font-size: $font-size-small;
}

.nav__link {
    color: $color-grey-100;
    font-weight: 450;
    margin: 0 8px;
    text-decoration: none;
}

.nav__link:hover {
    color: $color-green-500;
}
</style>