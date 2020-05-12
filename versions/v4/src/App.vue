<template>
  <div id="app">
    <!-- <NavBar /> -->
    <IntroSection />
    <AboutSection />
    <SkillsSection />
    <ProjectsSection />
    <InterestsSection />
    <MoreSection />
    <FooterSection />
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
import FooterSection from "@/sections/FooterSection.vue";
export default {
  name: 'App',
  components: {
    NavBar,
    IntroSection,
    AboutSection,
    SkillsSection,
    ProjectsSection,
    InterestsSection,
    MoreSection,
    FooterSection
  }
}
</script>

<style lang="scss">
@import "@/scss/global.scss";
</style>
