<template>
  <div class="featured-project">
    <img class="featured-project__image" :src="require(`../../assets/projects/${this.imgsrc}.jpg`)" />
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
import ProjectDetails from "./ProjectDetails.vue";
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
@import "@/scss/_mixins.scss";

$featured-project-img-width: 250px;
$featured-project-img-border: 2px solid $color-grey-100;

.featured-project {
  @include general-project-card;
  display: flex;
  margin-bottom: $spacing-section-small;

  &__image {
    width: $featured-project-img-width;
    border-top-left-radius: $border-radius-default;
    border-bottom-left-radius: $border-radius-default;
    border-right: $featured-project-img-border;
  }
}
</style>