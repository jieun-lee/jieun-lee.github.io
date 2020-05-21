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
@import "@/scss/_mediaquery.scss";

$featured-project-img-max-width: 475px;
$featured-project-img-width: 275px;
$featured-project-img-border: 2px solid $color-green-500;

.featured-project {
  @include general-project-card;
  display: flex;
  flex-direction: column;
  margin-bottom: $project-card-spacing;

  @include phablet-and-larger {
    flex-direction: row;
  }

  &__image {
    width: 92.5%;
    max-width: $featured-project-img-max-width;
    margin: 3.5vw auto 0;
    border: $featured-project-img-border;

    @include phablet-and-larger {
      width: $featured-project-img-width;
      margin: 0;
      border: none; // reset border
      border-top-left-radius: $border-radius-default;
      border-bottom-left-radius: $border-radius-default;
      border-right: $featured-project-img-border;
    }

    @include small-phone {
      display: none;
    }
  }
}
</style>