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
  background-color: $color-blue-lightest;
  margin-bottom: 16px;
  border-radius: $border-radius-default;

  &__image {
    max-width: 225px;
    border-top-left-radius: $border-radius-default;
    border-bottom-left-radius: $border-radius-default;
    border-right: 2px solid $color-grey-lighter;
  }
}
</style>