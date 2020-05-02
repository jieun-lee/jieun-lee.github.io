<template>
  <div id="app">
    <NavBar />
    <IntroSection />
    <AboutSection />
    <SkillsSection />
    <ProjectsSection />
    <InterestsSection />
    <MoreSection />
  </div>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import IntroSection from "@/sections/IntroSection.vue";
import AboutSection from "@/sections/AboutSection.vue";
import SkillsSection from "@/sections/SkillsSection.vue";
import ProjectsSection from "@/sections/ProjectsSection.vue";
import InterestsSection from "@/sections/InterestsSection.vue";
import MoreSection from "@/sections/MoreSection.vue";
export default {
  name: 'App',
  components: {
    NavBar,
    IntroSection,
    AboutSection,
    SkillsSection,
    ProjectsSection,
    InterestsSection,
    MoreSection
  }
}
</script>

<style lang="scss">
@import "@/scss/global.scss";
</style>
