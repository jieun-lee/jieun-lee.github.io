<template>
  <Section id="footer" theme="dark" :hideHeader="true">
    <div class="footer__content">
      &copy;2020 Jieun Lee
      <div class="footer__content__sub">
        Powered by Github Pages<br>
        Built with Vue.js
      </div>
    </div>
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

#footer {
  background-color: $color-grey-600;
  padding-bottom: $spacing-section-xsmall;
}

.footer__content {
  text-align: center;
  color: $color-grey-200;
  font-size: $font-size-default;

  &__sub {
    margin-top: $spacing-default;
    color: $color-grey-300;
    font-size: $font-size-small;
  }
}
</style>