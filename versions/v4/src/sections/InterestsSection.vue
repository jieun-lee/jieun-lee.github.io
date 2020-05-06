<template>
  <Section id="interests" theme="light">
    <div class="interests-wrapper">
      <InterestCardSub
        :name="this.interests[indexLeft]['name']"
        position="left"
        @interest-clicked="clicked('left')"
      />
      <InterestCardMid
        :name="this.interests[indexMid]['name']"
        :description="this.interests[indexMid]['description']"
        :link="this.interests[indexMid]['link']"
      />
      <InterestCardSub
        :name="this.interests[indexRight]['name']"
        position="right"
        @interest-clicked="clicked('right')"
      />
    </div>
  </Section>
</template>

<script>
import Section from "@/components/Section.vue";
import InterestCardSub from "@/components/InterestCardSub.vue";
import InterestCardMid from "@/components/InterestCardMid.vue";
import interestsData from "@/data/interests.json";
export default {
  components: {
    Section,
    InterestCardSub,
    InterestCardMid
  },
  data() {
    return {
      indexLeft: 0,
      numInterests: interestsData.interests.length,
      interests: interestsData.interests
    }
  },
  computed: {
    indexMid() {
      return (this.indexLeft + 1) % this.numInterests;
    },
    indexRight() {
      return (this.indexLeft + 2) % this.numInterests;
    }
  },
  methods: {
    clicked(side) {
      if (side === "right") {
        this.indexLeft = (this.indexLeft + 1) % this.numInterests;
      } else if (side === "left") {
        this.indexLeft = (this.indexLeft + this.numInterests - 1) % this.numInterests;
      }
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";

.interests-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>