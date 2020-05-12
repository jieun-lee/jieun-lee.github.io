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
  margin-top: 8px;
  display: flex;
  flex-wrap: wrap;

  &__skill {
    @include button-light(false);
    padding: 4px 8px;
    margin-right: 2px;
    margin-bottom: 2px;
    font-size: 12px;
    font-weight: 400;
  }
}
</style>