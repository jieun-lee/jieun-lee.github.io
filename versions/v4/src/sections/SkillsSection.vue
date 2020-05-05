<template>
  <Section id="skills" theme="light">
    <SkillsButtonBar @category-updated="updateCategory" />
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
export default {
  components: {
    Section,
    SkillsButtonBar,
    SkillItem
  },
  data() {
    return {
      category: "All",
      skills: [
        {name:"HTML", level:90, categories:['Web']},
        {name:"CSS/SCSS", level:90, categories:['Web']},
        {name:"JavaScript", level:85, categories:['Programming', 'Web']},
        {name:"Java", level:80, categories:['Programming', 'Mobile']},
        {name:"Vue.js", level:70, categories:['Web']},
        {name:"TypeScript", level:70, categories:['Programming', 'Web']},
        {name:"React Native", level:65, categories:['Mobile']},
        {name:"Python", level:60, categories:['Programming']},
        {name:"SQL", level:50, categories:['Other']},
        {name:"PHP", level:45, categories:['Web']},
        {name:"Node.js", level:35, categories:['Web']},
      ]
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