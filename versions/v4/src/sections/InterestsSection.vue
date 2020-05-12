<template>
  <Section id="interests" theme="dark">
    <div class="interests-wrapper interests-wrapper--main">
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
    <div class="interests-wrapper interests-wrapper--mini">
      <InterestCardMini
        v-for="interest in interests"
        :key="interest.name"
        :name="interest.name"
        :description="interest.description"
        :link="interest.link"
      />
    </div>
  </Section>
</template>

<script>
import Section from "@/components/Section.vue";
import InterestCardSub from "@/components/interests/InterestCardSub.vue";
import InterestCardMid from "@/components/interests/InterestCardMid.vue";
import InterestCardMini from "@/components/interests/InterestCardMini.vue";
import interestsData from "@/data/interests.json";
export default {
  components: {
    Section,
    InterestCardSub,
    InterestCardMid,
    InterestCardMini
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
@import "@/scss/_mediaquery.scss";

.interests-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;

  &--mini {
    flex-flow: wrap;
    align-items: stretch;
  }

  @include smaller-than-phablet {
    &--main {
      display: none;
    }
  }

  @include phablet-and-larger {
    &--mini {
      display: none;
    }
  }
}
</style>