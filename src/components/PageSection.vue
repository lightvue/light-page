<template>
  <section class="page-section">
    <div class="section-content" :class="{ '--full-width': fullWidth }">
      <slot></slot>
    </div>
  </section>
</template>

<script>
export default {
  props: ['fullWidth'],
}
</script>
