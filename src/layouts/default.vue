<template>
  <div>
    <app-header />
    <div class="page-container">
      <Nuxt />
    </div>
  </div>
</template>

<script>
import AppHeader from '@/components/AppHeader.vue';
export default {
  components: {
    AppHeader,
  },
};
</script>

<style lang="scss">
@import '@/assets/scss/global.scss';
</style>
