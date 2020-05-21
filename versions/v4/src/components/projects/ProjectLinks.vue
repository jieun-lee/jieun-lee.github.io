<template>
  <div class="project-links">
      <a
        v-if="this.code !== ''"
        :href="this.code"
        class="project-links__icon project-links__icon--code"
        target="_blank"
      >C</a>
      <a
        v-if="this.run !== ''"
        :href="this.run"
        class="project-links__icon project-links__icon--run"
        target="_blank"
      >R</a>
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

.project-links {
  display: flex;
  place-content: flex-end;
  margin-top: auto;

  &__icon {
    // later to be replaced with icons
    background-color: $color-green-500;
    border-radius: $border-radius-extra;
    padding: $spacing-xsmall $spacing-xsmall*2.5;
    text-align: center;
    text-decoration: none;
    color: $color-component-bg;
    font-weight: 600;
    margin-left: $spacing-xsmall;

    &:hover {
      background-color: $color-green-600;
    }
  }
}
</style>