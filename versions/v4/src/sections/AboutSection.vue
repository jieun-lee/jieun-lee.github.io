<template>
  <Section id="about" theme="light" :hideHeader="true">
    <AboutParagraph
      v-for="(paragraph, index) in paragraphs"
      :key="index"
      :header1="paragraph.header1"
      :header2="paragraph.header2"
      :paragraph="paragraph.paragraph"
      :isRight="index % 2 !== 0"
    />
  </Section>
</template>

<script>
import Section from "@/components/Section.vue";
import AboutParagraph from "@/components/about/AboutParagraph.vue";
import aboutData from "@/data/about.json";
export default {
  components: {
    Section,
    AboutParagraph
  },
  data() {
    return {
      paragraphs: aboutData.paragraphs
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
</style>