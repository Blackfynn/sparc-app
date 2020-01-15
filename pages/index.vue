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
  </div>
</template>

<script>
import BfButton from '@/components/shared/BfButton/BfButton.vue'
import PageHero from '@/components/PageHero/PageHero.vue'

export default {
  name: 'SparcHomepage',

  components: {
    BfButton,
    PageHero
  }
}
</script>

<style lang="scss" scoped>

</style>
