<template>
  <Section id="projects" theme="dark">
    <div class="projects-wrapper">
      <FeaturedProject
        v-for="project in featuredProjects"
        :key="project.name"
        :name="project.name"
        :imgsrc="project.imgsrc"
        :skills="project.skills"
        :description="project.description"
        :github="project.github"
        :playlink="project.playlink"
      />
    </div>
    <div class="projects-wrapper">
      <OtherProject
      v-for="project in otherProjects"
      :key="project.name"
      :name="project.name"
      :skills="project.skills"
      :description="project.description"
      :github="project.github"
      :playlink="project.playlink"
    />
    </div>
  </Section>
</template>

<script>
import Section from "@/components/Section.vue";
import FeaturedProject from "@/components/FeaturedProject.vue";
import OtherProject from "@/components/OtherProject.vue";
export default {
  components: {
    Section,
    FeaturedProject,
    OtherProject
  },
  data() {
    return {
      featuredProjects: [
        {
          name: "Type the Food",
          imgsrc: "type-the-food",
          skills: ["JavaScript", "CSS/SCSS", "HTML"],
          description: "Mini browser game involving memorizing short menus and typing",
          github: "https://github.com/jieun-lee/type-the-food",
          playlink: "https://jieun-lee.github.io/type-the-food/"
        },
        {
          name: "Ice Cream Game",
          imgsrc: "ice-cream-game",
          skills: ["Java", "Java Swing"],
          description: "Original Monopoly-like board game. Two players move around the board, buying ice cream flavours and collecting stars",
          github: "https://github.com/jieun-lee/ice-cream-game",
          playlink: ""
        },
        {
          name: "Mini Drum Kit",
          imgsrc: "mini-drum-kit",
          skills: ["JavaScript", "Vue.js", "CSS", "HTML"],
          description: "In-browser drum kit with a basic Kick, Snare, Hi-Hat, and Crash (sounds from Focusrite)",
          github: "https://github.com/jieun-lee/mini-drum-kit",
          playlink: "https://jieun-lee.github.io/mini-drum-kit/"
        },
      ],
      otherProjects: [
        {
          name: "Cookbook Database",
          skills: ["JavaScript", "PHP", "SQL", "CSS", "HTML"],
          description: "Group project for a databases course at school. A recipe database where users can upload their own recipes and manage their own cookbooks",
          github: "https://github.com/soohyunkim/Cookbook",
          playlink: "link"
        },
        {
          name: "Flying Vegetable",
          skills: ["Java", "Java Swing", "JavaScript", "HTML Canvas"],
          description: "V1 made with Java, V2 made with JavaScript. Mini game where a vegetable files up and down to avoid hitting obstacles",
          github: "https://github.com/jieun-lee/fly-vegetable",
          playlink: "https://jieun-lee.github.io/fly-vegetable/JavaScript/main.html"
        }
      ],
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";

.projects-wrapper {
  display: flex;
}
</style>