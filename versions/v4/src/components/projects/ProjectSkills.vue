<template>
  <div class="project-skills">
    <div v-for="(skill, index) in skills" :key="index" class="project-skills__skill">
      {{ skill }}
    </div>
  </div>
</template>

<script>
export default {
  props: {
    skills: Array
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
@import "@/scss/_mixins.scss";

.project-skills {
  margin-top: $spacing-small;
  display: flex;
  flex-wrap: wrap;

  &__skill {
    @include button-light(false);
    padding: $spacing-xsmall $spacing-small;
    margin-right: $spacing-xsmall;
    margin-bottom: $spacing-xsmall;
    font-size: $font-size-xsmall;
    font-weight: 400;
  }
}
</style>