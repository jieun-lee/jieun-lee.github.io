<template>
  <div
    class="skills-button"
    :class="[this.isSelected ? 'skills-button--selected' : '']"
    @click="onClick()">{{ type }}
  </div>
</template>

<script>
export default {
  props: {
    type: String,
    isSelected: Boolean
  },
  methods: {
    onClick() {
      // SkillsButtonBar is listening to this event
      this.$emit("skill-btn-clicked", this.type);
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
@import "@/scss/_mixins.scss";
.skills-button {
  margin: $spacing-xsmall;
  padding: $spacing-xsmall $spacing-default;

  &:not(&--selected) {
    @include button-dark;
  }

  &--selected {
    background-color: $color-green-800;
    border-radius: $border-radius-default;
    color: $color-grey-100;
    cursor: default;
  }
}
</style>