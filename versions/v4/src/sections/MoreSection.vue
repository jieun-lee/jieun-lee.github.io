<template>
  <Section id="more" theme="light" :hideHeader="true">
    Link to Github
    Link to LinkedIn
    Link to MyPortfolio
  </Section>
</template>

<script>
import Section from "@/components/Section.vue";
export default {
  components: {
    Section
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
</style>