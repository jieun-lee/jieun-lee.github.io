<template>
  <div class="featured-project">
    <img class="featured-project__image" :src="require(`../assets/projects/${this.imgsrc}.jpg`)" />
    <ProjectDetails
      :name="this.name"
      :skills="this.skills"
      :description="this.description"
      :links="this.links"
      :isFeatured="true"
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
    imgsrc: String,
    skills: Array,
    description: String,
    links: Object
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";

.featured-project {
  display: flex;
  background-color: $color-yellow-100;
  margin-bottom: 16px;
  border-radius: $border-radius-default;
  box-shadow: 4px 4px 0 0 $color-project-shadow;

  &__image {
    max-width: 250px;
    border-top-left-radius: $border-radius-default;
    border-bottom-left-radius: $border-radius-default;
    border-right: 2px solid $color-grey-100;
  }
}
</style>