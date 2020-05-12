<template>
  <div class="other-project">
    <ProjectDetails
      :name="this.name"
      :skills="this.skills"
      :description="this.description"
      :links="this.links"
      :isFeatured="false"
    />
  </div>
</template>

<script>
import ProjectDetails from "./ProjectDetails.vue";
export default {
  components: {
    ProjectDetails
  },
  props: {
    name: String,
    skills: Array,
    description: String,
    links: Object
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
@import "@/scss/_mixins.scss";

$other-project-min-height: 200px;

.other-project {
  @include general-project-card;
  padding: $spacing-default;
  min-height: $other-project-min-height;
  flex: 1 1 0;
  justify-content: space-between;

  &:not(:last-child) {
    margin-right: $spacing-large;
  }
}
</style>