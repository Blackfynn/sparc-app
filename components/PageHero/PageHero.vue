<template>
  <div class="page-hero">
    <el-row type="flex" justify="center">
      <el-col :xs="22" :sm="22" :md="22" :lg="20" :xl="18">
        <slot />
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'PageHero'
}
</script>

<style lang="scss">
.page-hero {
  background-image: linear-gradient(90deg, rgb(12, 0, 191) 0%, rgb(188, 0, 252) 100%);
  color: #f0f2f5;
  font-size: 1.625em;
  line-height: 2.375rem;
  padding: 3em 0;
  text-align: center;
}
</style>
