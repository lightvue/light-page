<template>
  <div>
    <page-section class="--dark-bg">
      <div class="dummy-block --x4"></div>
    </page-section>
    <page-section>
      <div class="flex-row --wrap dummy-flex-row">
        <div class="flex-item dummy-flex-item dummy-block --x3"></div>
        <div class="flex-item dummy-flex-item dummy-block --x3"></div>
        <div class="flex-item dummy-flex-item dummy-block --x3"></div>
      </div>
    </page-section>
    <page-section :fullWidth="true" class="--light-bg">
      <div class="dummy-block --x2"></div>
    </page-section>
    <page-section>
      <div class="dummy-block --x6"></div>
    </page-section>
    <page-section class="--dark-bg">
      <div class="flex-row --wrap dummy-flex-row">
        <div class="flex-item dummy-flex-item dummy-block --x3"></div>
        <div class="flex-item dummy-flex-item dummy-block --x3"></div>
        <div class="flex-item dummy-flex-item dummy-block --x3"></div>
      </div>
    </page-section>
    <page-section>
      <div class="dummy-block --x4"></div>
    </page-section>
    <page-section class="--dark-bg">
      <div class="flex-row --wrap dummy-flex-row">
        <div class="flex-item dummy-flex-item dummy-block --x3"></div>
        <div class="flex-item dummy-flex-item dummy-block --x3"></div>
        <div class="flex-item dummy-flex-item dummy-block --x3"></div>
        <div class="flex-item dummy-flex-item dummy-block --x3"></div>
      </div>
    </page-section>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import PageSection from '@/components/PageSection.vue'

export default Vue.extend({
  components: { PageSection },
})
</script>

<style lang="scss">
.--dark-bg {
  background-color: $color-bg-blue;
}
.--light-bg {
  background-color: $color-bg-light;
}
.dummy-block {
  width: 100%;
  height: 100px;
  background-color: rgba(0, 0, 0, 0.2);
  border-radius: 4px;
  &.--x2 {
    height: 200px;
  }
  &.--x3 {
    height: 300px;
  }
  &.--x4 {
    height: 400px;
  }
  &.--x5 {
    height: 500px;
  }
  &.--x6 {
    height: 600px;
  }
}
.dummy-flex-row {
  margin: -16px;
}
.dummy-flex-item {
  margin: 16px;
  min-width: 268px;
}
</style>
