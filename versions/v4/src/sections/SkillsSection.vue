<template>
  <Section id="skills" theme="light">
    Skills go Here
    <SkillBar name="Java" level=75 categories="['programming']" />
    <SkillBar name="JavaScript" level=80 categories="['programming', 'web']" />
  </Section>
</template>

<script>
import Section from "@/components/Section.vue";
import SkillBar from "@/components/SkillBar.vue";
export default {
  components: {
    Section,
    SkillBar
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
</style>