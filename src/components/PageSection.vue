<template>
  <section class="page-section" :class="{ '--allow-overflow': overflow }">
    <slot name="prepend"></slot>
    <div
      class="section-content"
      :class="{ '--full-width': fullWidth }"
      :style="{
        padding: padding,
        paddingTop: paddingY || paddingTop,
        paddingBottom: paddingY || paddingBottom,
      }"
    >
      <slot></slot>
    </div>
    <slot name="append"></slot>
  </section>
</template>

<script>
export default {
  props: {
    fullWidth: {
      type: Boolean,
      default: false,
    },
    overflow: {
      // default overflow-y will gets disturbed.
      type: Boolean,
      default: false,
    },
    padding: {
      type: String,
    },
    paddingY: {
      type: String,
    },
    paddingTop: {
      type: String,
    },
    paddingBottom: {
      type: String,
    },
  },
}
</script>
