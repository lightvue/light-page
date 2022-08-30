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

        paddingLeft: paddingX || paddingLeft,
        paddingRight: paddingX || paddingRight,
        margin: margin,
        marginTop: marginY || marginTop,
        marginBottom: marginY || marginBottom,
        marginLeft: marginX || marginLeft,
        marginRight: marginX || marginRight,
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

    paddingLeft: {
      type: String,
    },
    paddingRight: {
      type: String,
    },
    paddingX: {
      type: String,
    },
    margin: {
      type: String,
    },
    marginY: {
      type: String,
    },
    marginTop: {
      type: String,
    },
    marginBottom: {
      type: String,
    },
    marginLeft: {
      type: String,
    },
    marginRight: {
      type: String,
    },
    marginX: {
      type: String,
    },
  },
};
</script>
