<template>
  <div class="skills-button-bar">
    <SkillButton v-for="(type, index) in this.types"
      :key="index"
      :type="type"
      :isSelected="(selected === type)"
      @skill-btn-clicked="onButtonClick"
    />
  </div>
</template>

<script>
import SkillButton from "@/components/skills/SkillButton.vue";
import skillsData from "@/data/skills.json";
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
      types: skillsData.categories
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
    margin-top: -12px;
    margin-bottom: 24px;
  }
</style>