<template>
  <div class="project-details" :class="[ isFeatured ? 'project-details--featured' : '']">
    <div class="project-details__name">{{ this.name }}</div>
    <div class="project-details__description">{{ this.description }}</div>
  </div>
</template>

<script>
export default {
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

.project-details {
  padding: 8px 12px;

  &--featured {
    padding: 16px;
  }

  &__name {
    font-weight: 600;
    font-size: 18px;
  }

  &__description {
    font-size: 14px;
  }
}
</style>