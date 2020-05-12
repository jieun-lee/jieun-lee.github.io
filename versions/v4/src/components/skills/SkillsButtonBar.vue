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
@import "@/scss/_variables.scss";
@import "@/scss/_mediaquery.scss";

.skills-button-bar {
    display: flex;
    flex-direction: row;
    justify-content: center;
    flex-wrap: wrap;
    margin: -$spacing-default auto $spacing-section-xsmall;
    width: 75%;

    @include phablet-and-larger {
      width: 100%;
    }    
  }
</style>