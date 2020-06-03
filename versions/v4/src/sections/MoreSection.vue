<template>
  <Section id="more" theme="light" :hideHeader="true">
    <h2 class="more-section__header">External Links</h2>
    <div class="more-section__links">
      <a v-for="link in links"
        :key="link.name"
        :href="link.url"
        target="_blank"
        class="more-section__links__button"
      >
        {{ link.name }}
      </a>
    </div>
  </Section>
</template>

<script>
import Section from "@/components/Section.vue";
import linkData from "@/data/links.json";
export default {
  components: {
    Section
  },
  data() {
    return {
      links: linkData.links
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
@import "@/scss/_mixins.scss";
@import "@/scss/_mediaquery.scss";

.more-section {
  &__header {
    @include section-title;
    text-transform: uppercase;
  }

  &__links {
    display: flex;
    place-content: center;

    @include small-phone {
      flex-direction: column;
      width: 50%;
      margin: auto;
      text-align: center;
    }

    &__button {
      @include button-dark;
      border-radius: $border-radius-default * 1.5; // make rounder
      text-decoration: none;
      padding: $spacing-small $spacing-section-xsmall;
      margin: 0 $spacing-small;
      font-size: $font-size-large;

      @include small-phone {
        margin-bottom: $spacing-small;
        font-size: $font-size-default;
        padding: $spacing-small $spacing-large;
      }
    }
  }
}
</style>