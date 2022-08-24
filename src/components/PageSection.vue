<template>
  <section class="page-section" :class="{ '--allow-overflow': this.pageSection.overflow }">
    <slot name="prepend"></slot>
    <div
      class="section-content"
      :class="{ '--full-width': this.pageSection.fullWidth }"
      :style="{
        padding: this.pageSection.padding,
        paddingTop: this.pageSection.paddingY || this.pageSection.paddingTop,
        paddingBottom: this.pageSection.paddingY || this.pageSection.paddingBottom,
      }"
    >
      <slot></slot>
    </div>
    <slot name="append"></slot>
  </section>
</template>

<script>
export default {
  inject: ['pageSection'],
  // methods: {
  //   checkProp(prop, arg) {
  //     // this.count++;
  //     // console.log(this.count, ++this.count);
  //     console.log('called');
  //     // console.log(this[prop]);
  //     console.log(this.pageSection);
  //     // this[prop] === undefined ? (this.pageSection[prop] === '' ? arg : this.pageSection[prop]) : this[prop];
  //     return this[prop];
  //   },
  // },
};
</script>
