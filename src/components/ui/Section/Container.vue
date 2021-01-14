<template>
  <article class="container mx-auto py-16">
    <SectionTitle class="pb-8" :title="title"></SectionTitle>

    <div class="tracking-wider leading-loose">
      <slot></slot>
    </div>
  </article>
</template>

<script>
import SectionTitle from "./Title";

export default {
  components: {
    SectionTitle,
  },
  props: {
    title: {
      type: String,
      default: "Section Title",
    },
  },
};
</script>