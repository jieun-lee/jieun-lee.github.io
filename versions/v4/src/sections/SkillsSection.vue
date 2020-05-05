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
export default {
  components: {
    Section,
    SkillsButtonBar,
    SkillItem
  },
  data() {
    return {
      category: "Programming",
      skills: [
        {name:"HTML", level:90, categories:['Web']},
        {name:"CSS/SCSS", level:90, categories:['Web']},
        {name:"JavaScript", level:80, categories:['Programming', 'Web']},
        {name:"Java", level:75, categories:['Programming', 'Mobile']},
        {name:"Vue.js", level:70, categories:['Web']},
        {name:"jQuery", level:70, categories:['Web']},
        {name:"TypeScript", level:65, categories:['Programming', 'Web']},
        {name:"React", level:65, categories:['Web']},
        {name:"React Native", level:65, categories:['Mobile']},
        {name:"Jasmine", level:65, categories:['Web']},
        {name:"Git", level:60, categories:['Other']},
        {name:"Photoshop", level:60, categories:['Other']},
        {name:"Twig", level:55, categories:['Web']},
        {name:"Python", level:50, categories:['Programming']},
        {name:"SQL", level:50, categories:['Other']},
        {name:"ThreeJS", level:50, categories:['Web', 'Other']},
        {name:"PHP", level:40, categories:['Web']},
        {name:"Matlab", level:40, categories:['Other']},
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