<template>
  <div class="featured-datasets container">
    <el-row type="flex" justify="center">
      <el-col :xs="22" :sm="22" :md="22" :lg="20" :xl="18">
        <h2>News &amp; Upcoming Events</h2>
        <sparc-card
          image="https://placehold.it/544x394"
          image-alt="2020 SPARC Ideas Lab"
        >
          <h3>2020 SPARC Ideas Lab</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
            aliquip ex ea commodo consequat.
          </p>
          <p><a href="#">Learn More</a></p>
        </sparc-card>

        <sparc-card
          image="https://placehold.it/544x394"
          image-alt="2020 SPARC Ideas Lab"
          image-align="right"
        >
          <h3>2020 SPARC Ideas Lab</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
            aliquip ex ea commodo consequat.
          </p>
          <p><a href="#">Learn More</a></p>
        </sparc-card>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import SparcCard from '@/components/SparcCard/SparcCard.vue'

export default {
  name: 'HomepageNews',

  components: {
    SparcCard
  },

  data: function() {
    return {}
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/_variables.scss';
.sparc-card {
  margin-bottom: 24px;
  @media (min-width: 768px) {
    margin-bottom: 40px;
  }
}
</style>
