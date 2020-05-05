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
      this.$emit("clicked", this.type);
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
.skills-button {
  color: $color-grey-lightest;
  background-color: $color-blue-dark;
  border-radius: $border-radius-button;
  margin: 4px;
  padding: 4px 12px;

  &--selected {
    background-color: $color-blue-darker;
    cursor: default;
  }

  &:hover:not(&--selected) {
    background-color: $color-blue-base;
    cursor: pointer;
  }

}
</style>