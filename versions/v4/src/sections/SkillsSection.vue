<template>
  <Section id="skills" theme="light">
    <div class="skills__button-bar">
      <SkillButton type="All" />
      <SkillButton type="Programming" />
      <SkillButton type="Web" />
      <SkillButton type="Mobile" />
      <SkillButton type="Other" />
    </div>
    <SkillItem name="JavaScript" :level="80" :categories="['Programming', 'Web']" />
    <SkillItem name="Java" :level="75" :categories="['Programming', 'Mobile']" />
    <SkillItem name="React Native" :level="65" :categories="['Mobile']" />
    <SkillItem name="Node.js" :level="35" :categories="['Web']" />
  </Section>
</template>

<script>
import Section from "@/components/Section.vue";
import SkillButton from "@/components/SkillButton.vue";
import SkillItem from "@/components/SkillItem.vue";
export default {
  components: {
    Section,
    SkillButton,
    SkillItem
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";

.skills {
  &__button-bar {
    display: flex;
    flex-direction: row;
    justify-content: center;
  }
}
</style>