<template>
  <Section id="skills" theme="dark">
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
import SkillsButtonBar from "@/components/skills/SkillsButtonBar.vue";
import SkillItem from "@/components/skills/SkillItem.vue";
import skillsData from "@/data/skills.json";
export default {
  components: {
    Section,
    SkillsButtonBar,
    SkillItem
  },
  data() {
    return {
      category: "Featured",
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