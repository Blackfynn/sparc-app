<template>
  <div>
    <page-hero>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat.
      </p>
      <bf-button class="white">
        Browse All Data
      </bf-button>
    </page-hero>

    <featured-datasets />
  </div>
</template>

<script>
import BfButton from '@/components/shared/BfButton/BfButton.vue'
import FeaturedDatasets from '@/components/FeaturedDatasets/FeaturedDatasets.vue'
import PageHero from '@/components/PageHero/PageHero.vue'

export default {
  name: 'SparcHomepage',

  components: {
    BfButton,
    FeaturedDatasets,
    PageHero
  }
}
</script>

<style lang="scss" scoped>
::v-deep h2 {
  font-size: 1em;
  font-weight: 700;
  line-height: 2rem;
  @media (min-width: 768px) {
    font-size: 1.5em;
  }
}
</style>
