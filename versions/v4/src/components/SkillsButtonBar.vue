<template>
  <div class="skills-button-bar">
    <SkillButton v-for="(type, index) in this.types"
      :key="index"
      :type="type"
      :isSelected="(selected === type)"
      @clicked="onButtonClick"
    />
  </div>
</template>

<script>
import SkillButton from "@/components/SkillButton.vue";
export default {
  components: {
    SkillButton
  },
  props: {
    startCategory: String
  },
  data() {
    return {
      selected: this.startCategory,
      types: ["All", "Programming", "Web", "Mobile", "Other"]
    }
  },
  methods: {
    onButtonClick(value) {
      this.selected = value;
      this.$emit("category-updated", value);
    }
  }
}
</script>

<style lang="scss" scoped>
.skills-button-bar {
    display: flex;
    flex-direction: row;
    justify-content: center;
  }
</style>