<template>
  <article class="container mx-auto py-32">
    <SectionTitle v-if="$slots.title">
      <slot name="title"></slot>
    </SectionTitle>

    <SectionSubTitle v-if="$slots['sub-title']">
      <slot name="sub-title"></slot>
    </SectionSubTitle>

    <div class="mt-8 tracking-wider leading-loose">
      <slot></slot>
    </div>
  </article>
</template>

<script>
import SectionTitle from "./Title";
import SectionSubTitle from "./SubTitle";

export default {
  components: {
    SectionTitle,
    SectionSubTitle,
  },
};
</script>