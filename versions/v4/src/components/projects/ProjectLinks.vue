<template>
  <div class="project-links">
      <a v-if="this.code !== ''" :href="this.code" class="project-links__icon" target="_blank">
        <span class="project-links__icon__text project-links__icon__text--code">&lt;/&gt;</span>
      </a>
      <a v-if="this.run !== ''" :href="this.run" class="project-links__icon" target="_blank">
        <span class="project-links__icon__text project-links__icon__text--run">&#x25B6;</span>
      </a>
  </div>
</template>

<script>
export default {
  props: {
    links: Object
  },
  computed: {
    code() {
      return this.links.code || "";
    },
    run() {
      return this.links.run || "";
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";

$icon-dimensions: 32px;

.project-links {
  display: flex;
  place-content: flex-end;
  margin-top: auto;

  &__icon {
    // later to be replaced with icons
    background-color: $color-green-500;
    border-radius: $border-radius-extra;
    width: $icon-dimensions;
    height: $icon-dimensions;
    text-align: center;
    text-decoration: none;
    margin-left: $spacing-xsmall;
    position: relative;

    &__text {
      position: absolute;
      top: 50%;
      left: 50%;
      color: $color-component-bg;
      font-size: $font-size-xsmall;
      font-weight: 800;

      &--code {
        transform: translate(-50%, -55%);
      }

      &--run {
        transform: translate(-35%, -50%);
      }
    }

    &:hover {
      background-color: $color-green-600;
    }
  }
}
</style>