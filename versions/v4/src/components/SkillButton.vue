<template>
  <div class="skills-button">{{ type }}</div>
</template>

<script>
export default {
  props: {
    type: String
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
.skills-button {
  color: $color-grey-lightest;
  background-color: $color-blue-dark;
  border-radius: 12px;
  margin: 4px;
  padding: 4px 12px;
}
</style>