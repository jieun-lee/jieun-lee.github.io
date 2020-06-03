<template>
  <div class="project-details" :class="[ isFeatured ? 'project-details--featured' : '']">
    <div class="project-details__name">{{ this.name }}</div>
    <div class="project-details__description">{{ this.description }}</div>
    <ProjectSkills :skills="this.skills" />
    <ProjectLinks :links="this.links" />
  </div>
</template>

<script>
import ProjectSkills from "./ProjectSkills.vue";
import ProjectLinks from "./ProjectLinks.vue";
export default {
  components: {
    ProjectSkills,
    ProjectLinks
  },
  props: {
    name: String,
    skills: Array,
    description: String,
    links: Object,
    isFeatured: Boolean
  }
}
</script>>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
@import "@/scss/_mediaquery.scss";

$other-project-min-height: 200px;

.project-details {
  display: flex;
  flex-direction: column;

  &--featured {
    padding: $spacing-large;
  }

  @include phablet-and-larger {
    width: 100%;

    &:not(&--featured) {
      height: 100%;
    }
  }

  &__name {
    font-weight: 700;
    font-size: $font-size-large;

    @include phablet {
      font-size: $font-size-default;
    }
  }

  &__description {
    font-size: $font-size-small;

    @include phablet {
      font-size: $font-size-xsmall;
    }
  }
}
</style>