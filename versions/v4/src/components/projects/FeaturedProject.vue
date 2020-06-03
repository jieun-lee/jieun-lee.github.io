<template>
  <div class="featured-project">
    <div class="featured-project__image-wrapper">
      <img class="featured-project__image" :src="require(`../../assets/projects/${this.imgsrc}.jpg`)" />
    </div>
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
@import "@/scss/_mediaquery.scss";

$project-img-border-width: 2px;
$project-img-border: $project-img-border-width solid $color-green-500;

.featured-project {
  @include general-project-card;
  display: flex;
  flex-direction: column;
  margin-bottom: $project-card-spacing;

  @include phablet-and-larger {
    flex-direction: row;
  }

  &__image-wrapper {
    padding: $spacing-large;
    padding-bottom: 0;

    @include phablet-and-larger {
      padding: 0; // reset padding
      flex: 3 1 0;
      max-width: 300px;
    }
  }

  &__image {
    width: 100%;
    height: 100%;
    margin-left: -$project-img-border-width;
    margin-bottom: -$spacing-default;
    border: $project-img-border;

    @include phablet-and-larger {
      margin: 0; // reset margin
      border: none; // reset border
      border-top-left-radius: $border-radius-default;
      border-bottom-left-radius: $border-radius-default;
      border-right: $project-img-border;
    }
  }
}
</style>