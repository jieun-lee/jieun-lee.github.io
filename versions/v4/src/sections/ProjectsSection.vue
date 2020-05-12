<template>
  <Section id="projects" theme="light">
    <div class="featured-projects">
      <FeaturedProject
        v-for="project in featuredProjects"
        :key="project.name"
        :name="project.name"
        :imgsrc="project.imgsrc"
        :skills="project.skills"
        :description="project.description"
        :links="project.links"
      />
    </div>
    <div class="other-projects">
      <OtherProject
      v-for="project in otherProjects"
      :key="project.name"
      :name="project.name"
      :skills="project.skills"
      :description="project.description"
      :links="project.links"
    />
    </div>
  </Section>
</template>

<script>
import Section from "@/components/Section.vue";
import FeaturedProject from "@/components/projects/FeaturedProject.vue";
import OtherProject from "@/components/projects/OtherProject.vue";
import projectsData from "@/data/projects.json";
export default {
  components: {
    Section,
    FeaturedProject,
    OtherProject
  },
  data() {
    return {
      featuredProjects: projectsData.featured,
      otherProjects: projectsData.other,
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
@import "@/scss/_mediaquery.scss";

.other-projects {
  @include phablet-and-larger {
    display: flex;
  }
}
</style>