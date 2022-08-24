<template>
  <wrapper :class="['app-header__wrap']" :paddingY="paddingY">
    <div class="app-header flex-row --jc-between">
      <div class="app-header__logo-wrap">App Logo</div>
      <div class="app-header__center"></div>
      <div class="app-header__actions flex-row">
        <div class="dummy-action-item"></div>
        <div class="dummy-action-item"></div>
        <div class="dummy-action-item"></div>
      </div>
    </div>
  </wrapper>
</template>

<script>
import Wrapper from './Wrapper.vue';
export default {
  components: { Wrapper },
  data() {
    return {
      paddingY: '20px',
      properties: {
        fullWidth: 'false',
        overflow: 'true',
        padding: '20px',
        paddingY: '20px',
        paddingTop: '20px',
        paddingBottom: '20px',
      },
    };
  },
  provide() {
    return {
      wrapper: this.properties,
    };
  },
  mounted() {
    setTimeout(() => {
      console.log('called');
      this.paddingY = '100px';
    }, 3000);
  },
  // data() {
  //   return {
  //     py: '0px',
  //   };
  // },
};
</script>

<style lang="scss">
.app-header__wrap {
  position: fixed !important;
  left: 0px;
  top: 0px;
  z-index: 101;
  background-color: #fff;
  box-shadow: -4px 4px 6px -4px rgba(0, 0, 0, 0.15);
}
.app-header {
  height: $app-header-height;
  .app-header__logo-wrap {
    cursor: pointer;
    font-weight: 500;
    font-size: 24px;
    white-space: nowrap;
  }
  .app-header__actions {
  }
  .dummy-action-item {
    height: 32px;
    width: 32px;
    border-radius: 50%;
    cursor: pointer;
    margin-left: 12px;
    background-color: rgba(0, 0, 0, 0.1);
  }
}
</style>
