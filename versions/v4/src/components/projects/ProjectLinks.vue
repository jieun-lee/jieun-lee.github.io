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

  &__icon {
    background-color: $color-green-400;
    border-radius: 100px;
    padding: 4px 10px;
    text-align: center;
    text-decoration: none;
    color: $color-component-bg;
    font-weight: 600;
    margin-left: 4px;

    &:hover {
      background-color: $color-green-500;
    }
  }
}
</style>