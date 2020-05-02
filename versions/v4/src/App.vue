<template>
  <div id="app">
    <NavBar />
    <IntroSection />
    <AboutSection />
    <ProjectsSection />
    <SkillsSection />
  </div>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import IntroSection from "@/sections/IntroSection.vue";
import AboutSection from "@/sections/AboutSection.vue";
import ProjectsSection from "@/sections/ProjectsSection.vue";
import SkillsSection from "@/sections/SkillsSection.vue";
export default {
  name: 'App',
  components: {
    NavBar,
    IntroSection,
    AboutSection,
    ProjectsSection,
    SkillsSection
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
