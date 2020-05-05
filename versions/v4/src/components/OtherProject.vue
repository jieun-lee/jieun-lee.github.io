<template>
  <div class="other-project">
    {{ name }}
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    skills: Array,
    description: String,
    github: String,
    playlink: String
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";

.other-project {
  background-color: $color-blue-lightest;
  border-radius: $border-radius-default;
  padding: 12px;
  min-height: 200px;
  flex: 1 1 0;
  justify-content: space-between;

  &:not(:last-child) {
    margin-right: 16px;
  }
}
</style>