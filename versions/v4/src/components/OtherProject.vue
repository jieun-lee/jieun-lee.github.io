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
import ProjectDetails from "@/components/ProjectDetails.vue";
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

.other-project {
  background-color: $color-yellow-100;
  border-radius: $border-radius-default;
  padding: 12px;
  min-height: 200px;
  flex: 1 1 0;
  justify-content: space-between;
  box-shadow: 4px 4px 0 0 $color-project-shadow;

  &:not(:last-child) {
    margin-right: 16px;
  }
}
</style>