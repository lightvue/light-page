<template>
  <section class="page-section">
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
  </section>
</template>

<script>
export default {
  props: {
    fullWidth: {
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
