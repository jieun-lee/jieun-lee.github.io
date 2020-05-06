<template>
  <Section id="skills" theme="light">
    <SkillsButtonBar @category-updated="updateCategory" :startCategory="this.category" />
    <SkillItem
      v-for="(skill, index) in this.filteredSkills"
      :key="index"
      :name="skill.name"
      :level="skill.level"
      :categories="skill.categories"
    />
  </Section>
</template>

<script>
import Section from "@/components/Section.vue";
import SkillsButtonBar from "@/components/SkillsButtonBar.vue";
import SkillItem from "@/components/SkillItem.vue";
import skillsData from "@/data/skills.json";
export default {
  components: {
    Section,
    SkillsButtonBar,
    SkillItem
  },
  data() {
    return {
      category: "Programming",
      skills: skillsData.skills
    }
  },
  computed: {
    filteredSkills() {
      if (this.category === "All") {
        return this.skills;
      } else {
        return this.skills.filter((skill) => skill.categories.includes(this.category));
      }
    }
  },
  methods: {
    updateCategory(category) {
      this.category = category;
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
</style>