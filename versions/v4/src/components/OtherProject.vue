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
@import "@/scss/_mixins.scss";

.other-project {
  @include project-card;
}
</style>