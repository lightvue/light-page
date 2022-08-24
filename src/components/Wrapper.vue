<template>
  <page-section v-bind="$attrs">
    <template #prepend><slot name="prepend"></slot></template>
    <slot></slot>
    <template #append><slot name="append"></slot></template>
  </page-section>
</template>

<script>
import PageSection from './PageSection.vue';

export default {
  inheritAttrs: false,
  props: {
    fullWidth: {
      type: Boolean,
      // default: true,
    },
    overflow: {
      // default overflow-y will gets disturbed.
      type: Boolean,
      // default: true,
    },
    padding: {
      type: String,
    },
    paddingY: {
      type: String,
      // default: '20px',
    },
    paddingTop: {
      type: String,
    },
    paddingBottom: {
      type: String,
    },
  },
  components: { PageSection },
  data() {
    return {
      properties: {
        fullWidth: this.wrapper.fullWidth,
        overflow: this.wrapper.overflow,
        padding: this.wrapper.padding,
        paddingY: this.paddingY ? this.paddingY : this.wrapper.paddingY ? this.wrapper.paddingY : '100px',
        paddingTop: this.wrapper.paddingTop,
        paddingBottom: this.wrapper.paddingBottom,
      },
    };
  },
  provide() {
    return {
      pageSection: this.properties,
    };
  },
  inject: ['wrapper'],
};
</script>
