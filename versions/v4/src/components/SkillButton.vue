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
.skills-button {
  color: $color-grey-100;
  background-color: $color-green-500;
  border-radius: $border-radius-button;
  margin: 4px;
  padding: 4px 12px;

  &--selected {
    background-color: $color-green-800;
    cursor: default;
  }

  &:hover:not(&--selected) {
    background-color: $color-green-600;
    cursor: pointer;
  }

}
</style>